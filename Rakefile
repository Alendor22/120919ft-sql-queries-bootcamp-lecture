task :seed_data do
  puts "seeding data...."
  inject_database = "sqlite3 character_creator.db < "
  system(inject_database + "001_create_users.sql")
  system(inject_database + "002_create_characters.sql")
  system(inject_database + "003_insert_users.sql")
  system(inject_database + "004_insert_characters.sql")
end

task :open_db do
  puts "opening database..."
  system("sqlite3 character_creator.db")
end

task :reset_data do
  puts "resetting database..."
  system('rm character_creator.db')
  Rake::Task["seed_data"].execute
end

