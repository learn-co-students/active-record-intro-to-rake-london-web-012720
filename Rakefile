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
  require_relative './config/environment'
end


namespace :db do

  # task :environment do
  #   require_relative './config/environment'
  # end

  desc 'migrate changes to your database'
  task :migrate => :environment do #This creates a task dependency. Since our Student.create_table code would require access to the config/environment.rb
    Student.create_table
  end

  desc 'seed the database with some dummy data'
  task :seed do
    require_relative './db/seeds.rb'
  end

end

desc 'drop into the Pry console'
task :console => :environment do
  Pry.start
end
