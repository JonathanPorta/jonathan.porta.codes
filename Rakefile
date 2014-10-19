#!/usr/bin/env ruby

require 'html/proofer'



task default: %w[test]

# rake test
desc "html-proof the site"
task :test do
  HTML::Proofer.new("./_site", verbose: true, href_ignore: [/jonathanporta\.com/]).run
end

# rake build
desc "Build the site"
task :build do
  execute("jekyll build")
end

# == Helpers ===================================================================

# Execute a system command
def execute(command)
  system "#{command}"
end
