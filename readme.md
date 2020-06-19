## crete new site
* jekyll new site_name
## move into site directory
* cd site_name
## serve site
* for 1st run only -- bundle exec jekyll serve
* otherwise -- jekyll serve

## frontmatter
* it is the info about our blogpost -- i.e main info
* write either in yaml or json
* changing "category" can change url of post
* we can create our own variables as well

## more styling 
* we can create files in html instead of md directly

## organising
* make sub directories to organise
* it will not effect how jekyll renders pages

## drafts
* contains posts that are not yet published
* can be accessed by : jekyll serve --draft
* we may not name the draft with date in front
* it will automatically get last modified date

## pages
* 2 types of pages
** 1. general pages
** 2. posts
* eg. donate page in project root 
** /donate
* eg. support page in pagesdir folder
** /pagesdir/support

## permalink
* permanent url assigned to page of site
* so if date and title changes url remains same always
* eg. permalink: "put_url_here/url_here"
* eg. using some varible in url permalink: "/:categories/:year/:month:/title" 

## default frontmatter
* defined in config.yml to be set as default to some pages

## themes
* many themes available
* https://rubygems.org/search?utf8=%E2%9C%93&query=jekyll-theme
* eg. jekyll-theme-hacker --"add it to GemFile"
* bundle install -- to install the new theme
* change theme in config.yml
* themes may not have the layouts that you are using so update your layouts
 
## layouts
* we can override already given layouts from the theme
* eg. in layouts/page.html
* we can create levels of layout 

## variables
