django-blogs
===========

a django app for personal blog.

Quick start
-----------

* Install required packages

    ```shell
    $ pip install django-tinymce
    $ pip install BeautifulSoup
    $ pip install git+https://github.com/yijingping/django-blogs#egg=django_blogs
    ```

* Add "blogs" and "tinymce" to your INSTALLED_APPS setting like this

    ```python
    INSTALLED_APPS = (
        ...
        'tinymce',
        'blogs',
    )
    ```

* Include the blogs and tinymce URLconf in your project urls.py like this::

    ```python
    url(r'^tinymce/', include('tinymce.urls')),
    url(r'^/', include('blogs.urls')),  # route to blogs by default
    url(r'^blogs/', include('blogs.urls')),  # or route to blogs with 'blogs/' prefix 
    ```

* Run `python manage.py migrate` to create the blogs models.

* Start the development server and visit http://127.0.0.1:8000/admin/
   to create a blog (you'll need the Admin app enabled).

* Visit http://127.0.0.1:8000/ or /http://127.0.0.1:8000/blogs/ to view your blog home page.
