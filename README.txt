UiT-mal
-------

You can open index.html in your browser to see what the page will look
like.


Using the Templates
-------------------

All templates are combined in index.html. To use them in your project
you have to cut this file into pieces and make some minor
modifications to fit your template system.

* Copy the css and images directories to your project's static files
  directory.

* Cut index.html into header, navbar, banner and footer (the start of
  each is marked with "template: header" etc.) and put them in your
  template directory.

* Create a page template which includes the tempaltes. Django example::

    {% include 'header.html' %}
    {% include 'navbar.html' %}
    {% include 'banner.html' %}

    {% block content %}
    {% endblock %}

    {% if debug %}
      {% include 'debug.html' %}
    {% endif %}

    {% include 'footer.html' %}

* Change all variables to the syntax of your template engine. For example
  for Smarty change '{{ title }}' to '{$title}'.

* Replace links to index.php, hjelp.php and about.php with pages in
  your application.
