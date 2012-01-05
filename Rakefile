require "rubygems"
require "bundler"
Bundler.setup

# kludge to make it easier to use Bundler to find Alex's Showoff
task :showoff do
  args = ARGV[1..-1]
  exec("bundle exec showoff #{args.join(' ')} --split")
end
