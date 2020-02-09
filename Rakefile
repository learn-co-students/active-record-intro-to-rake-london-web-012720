namespace :greeting do
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc 'outputs hola to the terminal'
  task :hola do
    puts "hola de Rake!"
  end
end

desc 'console task'
task :console do
 puts 'hi'
end

desc 'require environment'
task :environment do
  require_relative './config/environment'
end

namespace :db do
  desc 'migrate changes to database'
  task :migrate => :environment do
    Student.create_table
  end

  desc 'seed database'
  task :seed do
    require_relative './db/seeds.rb'
  end
end

