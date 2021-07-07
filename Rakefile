desc 'outputs hello to the terminal'
task :hello do
  puts "hello from Rake!"
end

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

task :environment do
  require_relative "config/environment"
end  

namespace :db do

    desc 'migrate changes to your database'
    task :migrate => :environment do
      Student.create_table
    end

    desc ''
    task :seed do
      require_relative "db/seeds"
    end

end

desc "open up the console debug"
task :console => :environment do
  Pry.start
end