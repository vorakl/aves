
A theme for the Pelican (a static site generator) 
#################################################

:slug: info
:summary: A theme for the Pelican (a static site generator)

* About_
* Features_
* Installation_
* Examples_
* `A few words about index.html`_
* `A recommended minimum of variables and required values`_
* Screenshots_

About
=====

A theme for the Pelican_ (a static site generator).

It's based on the `tuxlite_tbs`_ theme but was significantly rewritten and extended by new features and customization.

Features
========

* Most of interface blocks such as a menu and a side bar, including their elements, can be turned on and off
* An archives index with links to years and months
* Lists of categories, tags, authors and pages with an elements' description as separate pages
* Lists of pages on a side bar 
* Configurable start page (what page to show if access the site's root)
* A compact paginator for the unlimited number of pages
* Provided configuration hides all html files in the end of links. All URLs end with a slash (e.g. site/path/to/)
* Any sub-directories along the path of URLs are accessable (e.g. site/tag/misc/ , site/tag/ , site/)
* A year in a copyright notice (`How to Write a Copyright Notice`_) is set dynamically and it depends on an entity: 
    + on group pages (tags, articles) it's set to dates of a first and a last articles
    + on a single page or article it's set to a creation date
* Versioning of static assets from the config file 
* Configurable header tags (``meta``) for SEO and a separate template for a favicon
* Shows avarage time to read an article
* Bonus:
    + a template of ``content`` directory and examples of configuration files for a tyical site
    + a simplified version of a Makefile (requires adjusting only a few path variables in a header) with a few features:
        - bundle CSS and JS files
        - build sites using dockerized Pelican
        - serve sites using dockerized Nginx
        - fallback to local/virtualenv Pelican with an integrated web server
        - one-liner to publish a site to a ``docs`` to the GitHub Pages in the same branch

Installation
============

The installation process is fairly trivial. Basically, you need only the `theme` directory from this repo. A path to it can be set in a few ways:

* in the ``THEMEDIR`` variable of the provided Makefile 
* in the ``-t /path/to/theme/`` command line option of ``pelican``
* in the ``THEME`` variable of ``pelicanconf.py``

This theme relies on a bunch of variables which are set in specific values. So, in addition, you need to adjust a configuration of your site accordingly to provided example files ``pelicanconf.py.example`` and ``publishconf.py.example``.

Examples
========

The example of a site's configuration with articles, pages, sitemap, robots.txt, favicon.ico, etc which is assumed to be used in GitHub Pages is presented in the `separate branch`__.

__ https://github.com/vorakl/aves/tree/example-site

Another examples of using this theme in live are

* `my blog`_ , as an example of using for blogging
* `TrivialRC's page`_ (`src`__), as an example of a project's site

__ https://github.com/vorakl/TrivialRC/tree/master/src.docs


A few words about index.html
============================

A list of articles is commonly placed in the root of the site in index.html. In this case, you cannot choose another start point, for example, some landing page. That's why I added a ``START_URL`` variale that specifies the URL to where a client will be redirected automatically from the root of the site. This is done by a simple ``start.html`` template. The original list of articles is intended to be placed in ``news/index.html``. Check ``TEMPLATE_PAGES`` and ``INDEX_SAVE_AS`` variables in the example configuration for details.


A recommended minimum of variables and required values
======================================================

A site will be rendered more or less right even without setting all these variables but it will not work as intended. To get most from this theme, it's recommended to set all of them and in proper values. Please, use examples as a base for the configuration of your site.

This theme brings new settings which are more suitable for using in ``pelicanconf.py``:

* ``SITEDESC``, a site's description
* ``CONTACT_URL``, a link to contacs of a site's owner
* ``START_URL``,  a start point of a site (like 'news/' or 'pages/about/')
* ``SITE_VERSION``, a version for static assets, e.g. js, css, ico
* ``SITE_KEYWORDS``, a list of key-words which appear in the html header
* ``DISPLAY_MENU``, all ``DISPLAY_*`` are self-explained and do what is expected
* ``DISPLAY_ITEMS_ON_MENU``
* ``DISPLAY_SIDEBAR``
* ``DISPLAY_ARCHIVES_ON_SIDEBAR``
* ``DISPLAY_CATEGORIES_ON_SIDEBAR``
* ``DISPLAY_PAGES_ON_SIDEBAR``
* ``DISPLAY_TAGS_ON_SIDEBAR``
* ``DISPLAY_AUTHORS_ON_SIDEBAR``
* ``DISPLAY_SUBSCRIBES_ON_SIDEBAR``
* ``DISPLAY_SITE_ON_SIDEBAR``
* ``DISPLAY_LINKS_ON_SIDEBAR``
* ``DISPLAY_AUTHOR``, adds an author in a article's metadata
* ``CATEGORIES_DESCRIPTION``, a list with categories and their short description. It's used in the list of categories
* ``TAGS_DESCRIPTION``, a list with tags and their short description. It's used in the list of tags
* ``FEED_EMAIL``, a link to e-mail subscription if it exists
* ``PAGES_SAVE_AS``, defines where to save a list of all pages
* ``PAGES_URL``, how to get a list of all pages

These existing variables should be present for a proper rendering (please, check appropriate values in example files):

* ``DEFAULT_PAGINATION``
* ``PAGINATION_PATTERNS``
* ``ARTICLE_SAVE_AS`` 
* ``ARTICLE_URL`` 
* ``ARTICLE_LANG_SAVE_AS`` 
* ``ARTICLE_LANG_URL`` 
* ``DRAFT_SAVE_AS`` 
* ``DRAFT_URL`` 
* ``DRAFT_LANG_SAVE_AS`` 
* ``DRAFT_LANG_URL`` 
* ``PAGE_SAVE_AS`` 
* ``PAGE_URL`` 
* ``PAGE_LANG_SAVE_AS`` 
* ``PAGE_LANG_URL`` 
* ``CATEGORY_SAVE_AS`` 
* ``CATEGORY_URL`` 
* ``TAG_SAVE_AS`` 
* ``TAG_URL`` 
* ``AUTHOR_SAVE_AS`` 
* ``AUTHOR_URL`` 
* ``INDEX_SAVE_AS`` 
* ``AUTHORS_SAVE_AS`` 
* ``AUTHORS_URL`` 
* ``ARCHIVES_SAVE_AS`` 
* ``ARCHIVES_URL`` 
* ``TAGS_SAVE_AS`` 
* ``TAGS_URL`` 
* ``CATEGORIES_URL`` 
* ``CATEGORIES_SAVE_AS`` 
* ``YEAR_ARCHIVE_SAVE_AS`` 
* ``MONTH_ARCHIVE_SAVE_AS`` 
* ``DAY_ARCHIVE_SAVE_AS``

Screenshots
===========

|screenshot-1|

|screenshot-2|

|screenshot-3|

|screenshot-4|

|screenshot-5|


.. Links

.. _Pelican: https://github.com/getpelican/pelican
.. _`tuxlite_tbs`: https://github.com/getpelican/pelican-themes/tree/master/tuxlite_tbs
.. _example: https://github.com/vorakl/aves/tree/example
.. _`my blog`: http://vorakl.name/
.. _`TrivialRC's page`: http://trivialrc.vorakl.name/
.. _`How to Write a Copyright Notice`: https://www.plagiarismtoday.com/2011/11/08/how-to-write-a-copyright-notice/

.. |screenshot-1| image:: {filename}/images/screenshot-1-news-desktop.png
   :alt: The main landing page with news
   :align: bottom
.. |screenshot-2| image:: {filename}/images/screenshot-2-article.png
   :alt: An example of an article page
   :align: bottom
.. |screenshot-3| image:: {filename}/images/screenshot-3-archive.png
   :alt: An archive index page
   :align: bottom
.. |screenshot-4| image:: {filename}/images/screenshot-4-authors-tablet.png
   :alt: An exmle of how Author's index looks like on tablets
   :align: bottom
.. |screenshot-5| image:: {filename}/images/screenshot-5-news-mobile.png
   :alt: The main landing page on a common mobile device
   :align: bottom

