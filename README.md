# Aves 

A theme for [Pelican](https://github.com/getpelican/pelican) (a static site generator).
It's based on the [tuxlite_tbs](https://github.com/getpelican/pelican-themes/tree/master/tuxlite_tbs) theme but was significantly rewritten and extended by new features and customization.

## Features

* Most of interface blocks such as a menu and a side bar, including their elements, can be turned on and off
* An archives index with links to years and months
* Lists of categories and tags with descriptions
* Configurable start page
* A paginator for the unlimited number of pages

## Installation

The installation process is fairly trivial. Just clone this repository and set a path to the theme's directory in the `THEME` variable of `pelicanconf.py`. This theme relies on a bunch of variables which are set in specific values. So, in addition, you need to adjust a configuration of your site accordingly to provided example files `pelicanconf.py.example` and `publishconf.py.example`.

## Example

The example of fully configured site with articles, pages, sitemap, robots.txt, favicon.ico, etc which is assumed to be used in GitHub Pages is presented at the separate branch [example]()

## index.html

A list of articles is commonly placed in the root of the site in index.html . In this case, you cannot choose another start point, for example, some landing page. That's why I added `START_URL` that specifies the URL to where a client will be redirected automatically from the root of the site. This is done by a simple start.html template. The original list of articles is intended to be placed in `news/index.html`. Check `TEMPLATE_PAGES` and `INDEX_SAVE_AS` variables in the example configuration for details.

## A recommended minimum of variables and required values

A site will be rendered more or less right even without setting all these variables but it will not work as intended. To get most from this theme, it's recommended to set all of them and in proper values. Please, use examples as a base for the configuration of your site.

This theme brings new settings which are more suitable for using in `pelicanconf.py`:

* `SITEDESC`, a site's description
* `CONTACT_URL`, a link to contacs of an owner of a site
* `START_URL`,  a start point of a site (like 'news/' or 'pages/about/')
* `DISPLAY_MENU`, all `DISPLAY_*` are self-explained and do what is expected
* `DISPLAY_ITEMS_ON_MENU`
* `DISPLAY_SIDEBAR`
* `DISPLAY_ARCHIVES_ON_SIDEBAR`
* `DISPLAY_CATEGORIES_ON_SIDEBAR`
* `DISPLAY_TAGS_ON_SIDEBAR`
* `DISPLAY_AUTHORS_ON_SIDEBAR`
* `DISPLAY_SUBSCRIBES_ON_SIDEBAR`
* `DISPLAY_SITE_ON_SIDEBAR`
* `DISPLAY_LINKS_ON_SIDEBAR`
* `DISPLAY_AUTHOR`, adds an author in a article's metadata
* `CATEGORIES_DESCRIPTION`, a list with categories and their short description. It's used in the list of categories
* `TAGS_DESCRIPTION`, a list with tags and their short description. It's used in the list of tags
* `FEED_EMAIL`, a link to e-mail subscription if it exists

These existing variables should be present for a proper rendering (please, check appropriate values in example files):

* `DEFAULT_PAGINATION`
* `PAGINATION_PATTERNS`
* `ARTICLE_SAVE_AS` 
* `ARTICLE_URL` 
* `ARTICLE_LANG_SAVE_AS` 
* `ARTICLE_LANG_URL` 
* `DRAFT_SAVE_AS` 
* `DRAFT_URL` 
* `DRAFT_LANG_SAVE_AS` 
* `DRAFT_LANG_URL` 
* `PAGE_SAVE_AS` 
* `PAGE_URL` 
* `PAGE_LANG_SAVE_AS` 
* `PAGE_LANG_URL` 
* `CATEGORY_SAVE_AS` 
* `CATEGORY_URL` 
* `TAG_SAVE_AS` 
* `TAG_URL` 
* `AUTHOR_SAVE_AS` 
* `AUTHOR_URL` 
* `INDEX_SAVE_AS` 
* `AUTHORS_SAVE_AS` 
* `AUTHORS_URL` 
* `ARCHIVES_SAVE_AS` 
* `ARCHIVES_URL` 
* `TAGS_SAVE_AS` 
* `TAGS_URL` 
* `CATEGORIES_URL` 
* `CATEGORIES_SAVE_AS` 
* `YEAR_ARCHIVE_SAVE_AS` 
* `MONTH_ARCHIVE_SAVE_AS` 
* `DAY_ARCHIVE_SAVE_AS`

