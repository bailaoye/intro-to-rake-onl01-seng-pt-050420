namespace :greeting do
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  task :hola do
    puts "hola de Rake!"
  end
end

desc 'requires env'
task :environment do
  require_relative './config/environment'
end

namespace :db do
  desc 'migrates changes to database'
  task :migrate => :environment do
    Student.create_table
  end

  desc 'seeds database with dummy data'
  task :seed do
    require_relative './db/seeds.rb'
  end
end

task :console => :environment do
  Pry.start
end