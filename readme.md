## install --on ubuntu
1. sudo apt-get install ruby-full build-essential zlib1g-dev
2. echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
3. echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
4. echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
5. source ~/.bashrc
6. gem install jekyll bundler

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
* can be accessed using {{}}

## includes
* header and footer 
* in "_includes" folder
* eg. {% include header.html %}
* eg. {% include header.html color="blue" %} --passing var to header

## looping posts
* eg. in home.html
{% for post in site.posts %}
<li><a href="{{ post.url }}">{{post.title}}</a></li> <br>
{% endfor %}

## conditionals
* eg. in post.html
* "and" , "or" for more conditions
{% if page.title == "this will override one as title" %}
<h3>if condition</h3>
{% elsif %}
<h3>yo</h3>
{% else %}
<h3>else condition</h3>
{% endif %}

## data files
* simple storage for our static file
* can be json / yml / csv etc.
* inside "_data" folder

## static files
* js, css, images for styling
* we can also give frontmatter to the static files -- in config.yml

## publish on github pages
* modify --config.yml
* baseurl: "your_repo_name" 
* or 
* baseurl: "put_your_custom_domain_name"
* git checkout -b gh-pages
* git status
* git push all files



