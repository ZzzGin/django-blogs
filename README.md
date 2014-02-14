django-blog
===========

a django app for personal blog.

Quick start
-----------

1. install required packages::

    $ pip install django-tinymce
    $ pip install BeautifulSoup
    $ pip install git+https://github.com/yijingping/django-blog#egg=django_blog

2. Add "blogs" and "tinymce" to your INSTALLED_APPS setting like this::

    INSTALLED_APPS = (
        ...
        'tinymce',
        'blogs',
    )

3. Include the blogs and tinymce URLconf in your project urls.py like this::

    url(r'^tinymce/', include('tinymce.urls')),
    url(r'^/', include('blogs.urls')),  # route to blogs by default
    url(r'^blogs/', include('blogs.urls')),  # or route to blogs with 'blogs/' prefix 

4. Run `python manage.py migrate` to create the blogs models.

5. Start the development server and visit http://127.0.0.1:8000/admin/
   to create a blog (you'll need the Admin app enabled).

6. Visit http://127.0.0.1:8000/ or /http://127.0.0.1:8000/blogs/ to view your blog home page.
