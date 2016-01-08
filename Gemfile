source 'https://rubygems.org'

require 'json'
require 'open-uri'
versions = JSON.parse(open('https://pages.github.com/versions.json').read)
gem 'jekyll', '2.4.0'
gem 'jekyll-sitemap'
gem 'jekyll-watch'
gem 'github-pages', versions['github-pages']
