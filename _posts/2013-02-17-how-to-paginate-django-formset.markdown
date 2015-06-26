---
layout: post
title: '[HOW TO] Paginate a Django formset'
date: '2013-02-17T18:41:00.000-03:00'
author: Filly
tags:
- tutorial
- software libre
- programación
modified_time: '2013-11-20T12:47:12.574-02:00'
blogger_id: tag:blogger.com,1999:blog-6145090415061302130.post-7527827415335907100
blogger_orig_url: http://missfillys.blogspot.com/2013/02/how-to-paginate-django-formset.html
---
Last month I needed to paginate a Django model formset and I couldn't find the way to do it, but I found posts asking
the same question without an answer, so here is my solution:  

In the `forms.py` file:

{% highlight python %}
class MyForm(ModelForm):  
    class Meta:  
        model = MyModel  
        fields = ('description',)
{% endhighlight %}

In the `views.py` file:  

{% highlight python %}
FormSet = modelformset_factory(MyModel, form=MyForm, extra=0)  
if request.method == 'POST':  
    formset = FormSet(request.POST, request.FILES)  
    if formset.is_valid():  
        formset.save()  
    return HttpResponse('Formset submited!')  
else:  
    query = MyModel.objects.filter(condition)  
    paginator = Paginator(query, 10)  # Show 10 forms per page  
    page = request.GET.get('page')  
    try:  
        objects = paginator.page(page)  
    except PageNotAnInteger:  
        objects = paginator.page(1)  
    except EmptyPage:  
        objects = paginator.page(paginator.num_pages)  
    page_query = MyModel.objects.filter(id__in=[object.id for object in objects])  
    formset = FormSet(queryset=page_query)  
    context = {'objects': objects, 'formset': formset}  
    return render_to_response('template.html', context,  
                              context_instance=RequestContext(request))
{% endhighlight %}

You need to create the formset with the objects in the present page, otherwise, when you try to do
`formset = FormSet(request.POST, request.FILES)` in the `POST` method, Django raises a `MultiValueDictKeyError error`.  

In the `template.html` file:  

{% highlight html%}
{% raw %}

{% extends "base.html" %}
{% block content %}
<h1>Paginated formset</h1>
{% if objects %}
    <form action="" method="post">
        {% csrf_token %}
        {{ formset.management_form }}
        {% for form in formset.forms %}
            {{ form.id }}
            <div class="object-frame">
                <div class="object">
                    <p><span>Name: </span>{{ form.instance.name }}</p>
                    {{ form.as_p }}
                </div>
            </div>
        {% endfor %}
        <input value="Save" type="submit">
    </form>
 
    <div class="pagination">
        <span class="step-links">
            {% if objects.has_previous %}
                <a href="?page={{ objects.previous_page_number }}">Previous</a>
            {% endif %}
 
            <span class="current">
                Page {{ objects.number }} of {{ objects.paginator.num_pages }}
            </span>
 
            {% if objects.has_next %}
                <a href="?page={{ objects.next_page_number }}">next</a>
            {% endif %}
        </span>
    </div>
{% else %}
    <p>There are no objects.</p>
{% endif %}
{% endblock %}

{% endraw %}
{% endhighlight %}