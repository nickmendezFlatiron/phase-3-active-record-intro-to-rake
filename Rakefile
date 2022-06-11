task :environment do
  require_relative './config/environment'
end 

desc 'drop into the Pry Console'
task console: :environment do
  Pry.start
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

namespace :db do
  desc 'migrate changes to your db'
  task migrate: :environment do
    Student.create_table
  end

  desc 'seeds data with sime dummy data'
  task seed: :environment do
    require_relative './db/seeds'
  end 
end 