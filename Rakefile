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

desc 'starts a console'
task :console do
  ActiveRecord::Base.logger = Logger.new(STDOUT)
  Pry.start
end

desc 'adds environment file'
task :environment do
  require_relative './config/environment'
end

namespace :db do
  desc 'migrate changes to your database'
  task :migrate => :environment do
    Student.create_table
  end

   
  desc 'seed the database with some dummy data'
  task :seed do
    require_relative './db/seeds.rb'
  end
  
end