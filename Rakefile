# Add your own tasks in files placed in lib/tasks ending in .rake,
# for example lib/tasks/capistrano.rake, and they will automatically be available to Rake.

require_relative "config/application"

Rails.application.load_tasks

# Fake precompilation, we assert it's called...it's the user's responsibility to make
# sure what happens after that works.
["assets:precompile", "assets:clean"].each do |name|
  Rake::Task[name].clear
  task name do
    puts "Ran #{name}"
  end
end
