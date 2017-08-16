Jekyll Categories
=================

This gem provides a [Jekyll](http://github.com/mojombo/jekyll) generator for
category pages, category feeds and a category index.

# Basic Setup

Add the gem in your Gemfile:

```ruby
group :jekyll_plugins do
  gem 'jekyll-feed', '~> 0.6'
  gem 'jekyll-categories'
end
```

Add the plugin in the `_config.yml`:

```yaml
plugins:
  - jekyll-feed
  - jekyll-categories
```

Create the following layouts:

- category_index.html (For creating an index for each category)
- category_list.html (For creating the categories list)
- category_feed.xml (For the [Atom feed](https://en.wikipedia.org/wiki/Atom_(standard)))

# Filters
This gem comes with the following filters.

## category_url
Allows you to get the url of a given category.

```html
{% for category in site.categories %}
  <li><a href="{% category_url category.first %}">{{ category.first }}</a></li>
{% endfor %}
```
