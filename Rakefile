#!/usr/bin/env ruby

require 'html/proofer'

task default: %w[test]

# rake test
desc "html-proof the site"
task :test do
  HTML::Proofer.new("./_site", href_ignore: [/jonathan\.porta\.codes/, /\#/]).run
end

# rake build
desc "Build the site"
task :build do
  execute("jekyll build")
end

# rake serve
desc "Build and Serve the site"
task :serve do
  execute("jekyll serve")
end

desc "Create a new post"
task :post do
  today = Date.today
  title = ENV['TITLE']

  slug = slugify title
  permalink = permalinkify today, slug

  file = filename today, slug

  File.open(file, "w") do |fp|
    fp << <<-EOS.gsub(/^    /, '')
    ---
    layout: post
    title:  "#{ title }"
    date:   #{ today }
    categories:
    permalink: #{ permalink }
    comments: true
    ---

    EOS
  end

  puts "-------------\n"
  puts "Post Created!\n"
  puts "-------------\n"
  puts "Title: #{ title }\n"
  puts "Slug: #{ slug }\n"
  puts "Permalink: #{ permalink }\n"
  puts "Filename: #{ file }\n"
end

# == Helpers ===================================================================

# Execute a system command
def execute(command)
  system "#{ command }"
end

def permalinkify(date, slug)
  year = date.strftime '%Y'
  month = date.strftime '%m'
  day = date.strftime '%d'

  "/#{ year }/#{ month }/#{ day }/#{ slug }"
end

def slugify(title)
  "#{ title.downcase.gsub(/[^\w]+/, '-') }"
end

def filename(date, slug)
  File.join(File.dirname(__FILE__), '_posts', "#{ date }-#{ slug }" + '.markdown')
end
