task :teachers do
  unless File.exist?('Gemfile.lock')
    system("bundle") or raise("Unable to bundle, run bundle directly to see what's what.")
  end
  exec("bundle && bundle exec showoff serve teachers")
end