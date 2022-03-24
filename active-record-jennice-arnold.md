<!-- Console log of the rolodex challenge exercise: -->
learnacademy@LEARNs-Air database-challenges % rails new rolodex_challenge -d postgresql -T
      create  
      create  README.md
      create  Rakefile
      create  .ruby-version
      create  config.ru
      create  .gitignore
      create  .gitattributes
      create  Gemfile
         run  git init from "."
hint: Using 'master' as the name for the initial branch. This default branch name
hint: is subject to change. To configure the initial branch name to use in all
hint: of your new repositories, which will suppress this warning, call:
hint: 
hint: 	git config --global init.defaultBranch <name>
hint: 
hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
hint: 'development'. The just-created branch can be renamed via this command:
hint: 
hint: 	git branch -m <name>
Initialized empty Git repository in /Users/learnacademy/Desktop/LEARN/database-challenges/rolodex_challenge/.git/
      create  app
      create  app/assets/config/manifest.js
      create  app/assets/stylesheets/application.css
      create  app/channels/application_cable/channel.rb
      create  app/channels/application_cable/connection.rb
      create  app/controllers/application_controller.rb
      create  app/helpers/application_helper.rb
      create  app/jobs/application_job.rb
      create  app/mailers/application_mailer.rb
      create  app/models/application_record.rb
      create  app/views/layouts/application.html.erb
      create  app/views/layouts/mailer.html.erb
      create  app/views/layouts/mailer.text.erb
      create  app/assets/images
      create  app/assets/images/.keep
      create  app/controllers/concerns/.keep
      create  app/models/concerns/.keep
      create  bin
      create  bin/rails
      create  bin/rake
      create  bin/setup
      create  config
      create  config/routes.rb
      create  config/application.rb
      create  config/environment.rb
      create  config/cable.yml
      create  config/puma.rb
      create  config/storage.yml
      create  config/environments
      create  config/environments/development.rb
      create  config/environments/production.rb
      create  config/environments/test.rb
      create  config/initializers
      create  config/initializers/assets.rb
      create  config/initializers/content_security_policy.rb
      create  config/initializers/cors.rb
      create  config/initializers/filter_parameter_logging.rb
      create  config/initializers/inflections.rb
      create  config/initializers/new_framework_defaults_7_0.rb
      create  config/initializers/permissions_policy.rb
      create  config/locales
      create  config/locales/en.yml
      create  config/master.key
      append  .gitignore
      create  config/boot.rb
      create  config/database.yml
      create  db
      create  db/seeds.rb
      create  lib
      create  lib/tasks
      create  lib/tasks/.keep
      create  lib/assets
      create  lib/assets/.keep
      create  log
      create  log/.keep
      create  public
      create  public/404.html
      create  public/422.html
      create  public/500.html
      create  public/apple-touch-icon-precomposed.png
      create  public/apple-touch-icon.png
      create  public/favicon.ico
      create  public/robots.txt
      create  tmp
      create  tmp/.keep
      create  tmp/pids
      create  tmp/pids/.keep
      create  tmp/cache
      create  tmp/cache/assets
      create  vendor
      create  vendor/.keep
      create  storage
      create  storage/.keep
      create  tmp/storage
      create  tmp/storage/.keep
      remove  config/initializers/cors.rb
      remove  config/initializers/new_framework_defaults_7_0.rb
         run  bundle install
Fetching gem metadata from https://rubygems.org/...........
Fetching gem metadata from https://rubygems.org/.
Resolving dependencies...........
Using rake 13.0.6
Using concurrent-ruby 1.1.9
Using websocket-extensions 0.1.5
Using marcel 1.0.2
Using mini_mime 1.1.2
Using digest 3.1.0
Using io-wait 0.2.1
Using crass 1.0.6
Using strscan 3.0.1
Using bindex 0.8.1
Using builder 3.2.4
Using bundler 2.2.3
Using io-console 0.5.11
Using method_source 1.0.0
Using rack 2.2.3
Using zeitwerk 2.5.4
Using minitest 5.15.0
Using erubi 1.10.0
Using tzinfo 2.0.4
Using websocket-driver 0.7.5
Using mail 2.7.1
Using reline 0.3.1
Using thor 1.2.1
Fetching i18n 1.10.0
Fetching pg 1.3.4
Fetching sprockets 4.0.3
Fetching msgpack 1.4.5
Using timeout 0.2.0
Using irb 1.4.1
Using net-protocol 0.1.2
Using debug 1.4.0
Using net-imap 0.2.3
Using net-pop 0.1.1
Using net-smtp 0.3.1
Using rack-test 1.1.0
Using nio4r 2.5.8
Using racc 1.6.0
Fetching puma 5.6.2
Fetching nokogiri 1.13.3 (x86_64-darwin)
Installing i18n 1.10.0
Installing msgpack 1.4.5 with native extensions
Installing sprockets 4.0.3
Installing pg 1.3.4 with native extensions
Installing puma 5.6.2 with native extensions
Fetching activesupport 7.0.2.3
Installing activesupport 7.0.2.3
Using globalid 1.0.0
Fetching activemodel 7.0.2.3
Fetching activejob 7.0.2.3
Installing activejob 7.0.2.3
Installing activemodel 7.0.2.3
Fetching activerecord 7.0.2.3
Installing activerecord 7.0.2.3
Installing nokogiri 1.13.3 (x86_64-darwin)
Using rails-dom-testing 2.0.3
Fetching loofah 2.15.0
Installing loofah 2.15.0
Using rails-html-sanitizer 1.4.2
Fetching actionview 7.0.2.3
Installing actionview 7.0.2.3
Using jbuilder 2.11.5
Fetching actionpack 7.0.2.3
Installing actionpack 7.0.2.3
Using sprockets-rails 3.4.2
Fetching activestorage 7.0.2.3
Fetching actionmailer 7.0.2.3
Fetching actioncable 7.0.2.3
Fetching railties 7.0.2.3
Installing actionmailer 7.0.2.3
Installing actioncable 7.0.2.3
Installing activestorage 7.0.2.3
Installing railties 7.0.2.3
Fetching actiontext 7.0.2.3
Fetching actionmailbox 7.0.2.3
Installing actionmailbox 7.0.2.3
Installing actiontext 7.0.2.3
Using turbo-rails 1.0.1
Using web-console 4.2.0
Fetching importmap-rails 1.0.3
Fetching rails 7.0.2.3
Fetching stimulus-rails 1.0.4
Installing rails 7.0.2.3
Installing stimulus-rails 1.0.4
Installing importmap-rails 1.0.3
Fetching bootsnap 1.11.1
Installing bootsnap 1.11.1 with native extensions
Bundle complete! 12 Gemfile dependencies, 63 gems now installed.
Use `bundle info [gemname]` to see where a bundled gem is installed.
         run  bundle binstubs bundler
       rails  importmap:install
Add Importmap include tags in application layout
      insert  app/views/layouts/application.html.erb
Create application.js module as entrypoint
      create  app/javascript/application.js
Use vendor/javascript for downloaded pins
      create  vendor/javascript
      create  vendor/javascript/.keep
Ensure JavaScript files are in the Sprocket manifest
      append  app/assets/config/manifest.js
Configure importmap paths in config/importmap.rb
      create  config/importmap.rb
Copying binstub
      create  bin/importmap
       rails  turbo:install stimulus:install
Import Turbo
      append  app/javascript/application.js
Pin Turbo
      append  config/importmap.rb
Run turbo:install:redis to switch on Redis and use it in development for turbo streams
Create controllers directory
      create  app/javascript/controllers
      create  app/javascript/controllers/index.js
      create  app/javascript/controllers/application.js
      create  app/javascript/controllers/hello_controller.js
Import Stimulus controllers
      append  app/javascript/application.js
Pin Stimulus
Appending: pin "@hotwired/stimulus", to: "stimulus.min.js", preload: true"
      append  config/importmap.rb
Appending: pin "@hotwired/stimulus-loading", to: "stimulus-loading.js", preload: true
      append  config/importmap.rb
Pin all controllers
Appending: pin_all_from "app/javascript/controllers", under: "controllers"
      append  config/importmap.rb
learnacademy@LEARNs-Air database-challenges % ls
README.md		rolodex_challenge
learnacademy@LEARNs-Air database-challenges % cd rolodex_challenge
learnacademy@LEARNs-Air rolodex_challenge % rails db:create
Created database 'rolodex_challenge_development'
Created database 'rolodex_challenge_test'
learnacademy@LEARNs-Air rolodex_challenge % rails server
=> Booting Puma
=> Rails 7.0.2.3 application starting in development 
=> Run `bin/rails server --help` for more startup options
Puma starting in single mode...
* Puma version: 5.6.2 (ruby 3.0.0-p0) ("Birdie's Version")
*  Min threads: 5
*  Max threads: 5
*  Environment: development
*          PID: 30021
* Listening on http://127.0.0.1:3000
* Listening on http://[::1]:3000
Use Ctrl-C to stop
Started GET "/" for ::1 at 2022-03-17 16:13:49 -0700
Processing by Rails::WelcomeController#index as HTML
  Rendering /Users/learnacademy/.rvm/gems/ruby-3.0.0/gems/railties-7.0.2.3/lib/rails/templates/rails/welcome/index.html.erb
  Rendered /Users/learnacademy/.rvm/gems/ruby-3.0.0/gems/railties-7.0.2.3/lib/rails/templates/rails/welcome/index.html.erb (Duration: 8.4ms | Allocations: 746)
Completed 200 OK in 77ms (Views: 28.7ms | ActiveRecord: 0.0ms | Allocations: 7046)


rails
test
rails l
^C- Gracefully stopping, waiting for requests to finish
=== puma shutdown: 2022-03-17 16:19:56 -0700 ===
- Goodbye!
Exiting
learnacademy@LEARNs-Air rolodex_challenge % rails generate model Person first_name:string last_name:string phone:string
      invoke  active_record
      create    db/migrate/20220317232224_create_people.rb
      create    app/models/person.rb
learnacademy@LEARNs-Air rolodex_challenge % rails db:migrate
== 20220317232224 CreatePeople: migrating =====================================
-- create_table(:people)
   -> 0.0317s
== 20220317232224 CreatePeople: migrated (0.0320s) ============================

learnacademy@LEARNs-Air rolodex_challenge % ls
Gemfile		Rakefile	config		lib		storage
Gemfile.lock	app		config.ru	log		tmp
README.md	bin		db		public		vendor
learnacademy@LEARNs-Air rolodex_challenge % cd app
learnacademy@LEARNs-Air app % ls
assets		controllers	javascript	mailers		views
channels	helpers		jobs		models
learnacademy@LEARNs-Air app % cd models
learnacademy@LEARNs-Air models % ls
application_record.rb	concerns		person.rb
learnacademy@LEARNs-Air models % code .
learnacademy@LEARNs-Air models % rails c
Loading development environment (Rails 7.0.2.3)
3.0.0 :001 > Person.create first_name: "Gon", last_name: "Freaks", phone: "61901
2345"
  TRANSACTION (9.2ms)  BEGIN
  Person Create (7.9ms)  INSERT INTO "people" ("first_name", "last_name", "phone", "created_at", "updated_at") VALUES ($1, $2, $3, $4, $5) RETURNING "id"  [["first_name", "Gon"], ["last_name", "Freaks"], ["phone", "619012345"], ["created_at", "2022-03-17 23:36:37.710193"], ["updated_at", "2022-03-17 23:36:37.710193"]] 
  TRANSACTION (4.1ms)  COMMIT                                                   
 =>                                                                             
#<Person:0x00007fa187611568                                                     
 id: 1,                                                                         
 first_name: "Gon",                                                             
 last_name: "Freaks",                                                           
 phone: "619012345",                                                            
 created_at: Thu, 17 Mar 2022 23:36:37.710193000 UTC +00:00,                    
 updated_at: Thu, 17 Mar 2022 23:36:37.710193000 UTC +00:00>                    
3.0.0 :002 > Person.create first_name: "Midoriya", last_name: "Izuku", phone: "8
004156000"
  TRANSACTION (23.3ms)  BEGIN
  Person Create (1.2ms)  INSERT INTO "people" ("first_name", "last_name", "phone", "created_at", "updated_at") VALUES ($1, $2, $3, $4, $5) RETURNING "id"  [["first_name", "Midoriya"], ["last_name", "Izuku"], ["phone", "8004156000"], ["created_at", "2022-03-17 23:39:01.596987"], ["updated_at", "2022-03-17 23:39:01.596987"]]                                                                            
  TRANSACTION (2.1ms)  COMMIT                                                   
 =>                                                                             
#<Person:0x00007fa185b0aff8                                                     
 id: 2,                                                                         
 first_name: "Midoriya",                                                        
 last_name: "Izuku",                                                            
 phone: "8004156000",                                                           
 created_at: Thu, 17 Mar 2022 23:39:01.596987000 UTC +00:00,                    
 updated_at: Thu, 17 Mar 2022 23:39:01.596987000 UTC +00:00> 
3.0.0 :003 > Person.create first_name: "Hayao", last_name: "Miyazaki", phone: "8
1570055777"
  TRANSACTION (4.8ms)  BEGIN
  Person Create (0.5ms)  INSERT INTO "people" ("first_name", "last_name", "phone", "created_at", "updated_at") VALUES ($1, $2, $3, $4, $5) RETURNING "id"  [["first_name", "Hayao"], ["last_name", "Miyazaki"], ["phone", "81570055777"], ["created_at", "2022-03-17 23:41:21.662260"], ["updated_at", "2022-03-17 23:41:21.662260"]]                                                                           
  TRANSACTION (1.0ms)  COMMIT                                                   
 =>                                                                             
#<Person:0x00007fa186a88a20                                                     
 id: 3,                                                                         
 first_name: "Hayao",                                                           
 last_name: "Miyazaki",                                                         
 phone: "81570055777",                                                          
 created_at: Thu, 17 Mar 2022 23:41:21.662260000 UTC +00:00,                    
 updated_at: Thu, 17 Mar 2022 23:41:21.662260000 UTC +00:00> 
3.0.0 :004 > Person.create first_name: "Borrito", last_name: "Uzumaki", phone: "
50050005000"
  TRANSACTION (0.2ms)  BEGIN
  Person Create (0.5ms)  INSERT INTO "people" ("first_name", "last_name", "phone", "created_at", "updated_at") VALUES ($1, $2, $3, $4, $5) RETURNING "id"  [["first_name", "Borrito"], ["last_name", "Uzumaki"], ["phone", "50050005000"], ["created_at", "2022-03-17 23:43:24.668747"], ["updated_at", "2022-03-17 23:43:24.668747"]]                                                                          
  TRANSACTION (1.1ms)  COMMIT                                                   
 =>                                                                             
#<Person:0x00007fa185282cf0                                                     
 id: 4,                                                                         
 first_name: "Borrito",                                                         
 last_name: "Uzumaki",                                                          
 phone: "50050005000",                                                          
 created_at: Thu, 17 Mar 2022 23:43:24.668747000 UTC +00:00,                    
 updated_at: Thu, 17 Mar 2022 23:43:24.668747000 UTC +00:00> 
3.0.0 :005 > Person.create first_name: "Ash", last_name: "Ketchum", phone: "0000
00000"
  TRANSACTION (1.9ms)  BEGIN
  Person Create (0.7ms)  INSERT INTO "people" ("first_name", "last_name", "phone", "created_at", "updated_at") VALUES ($1, $2, $3, $4, $5) RETURNING "id"  [["first_name", "Ash"], ["last_name", "Ketchum"], ["phone", "000000000"], ["created_at", "2022-03-17 23:44:03.661965"], ["updated_at", "2022-03-17 23:44:03.661965"]]
  TRANSACTION (0.9ms)  COMMIT                                                   
 =>                                                                             
#<Person:0x00007fa18556b7a0                                                     
 id: 5,                                                                         
 first_name: "Ash",                                                             
 last_name: "Ketchum",                                                          
 phone: "000000000",                                                            
 created_at: Thu, 17 Mar 2022 23:44:03.661965000 UTC +00:00,                    
 updated_at: Thu, 17 Mar 2022 23:44:03.661965000 UTC +00:00>                    
3.0.0 :006 > Person.all
  Person Load (16.5ms)  SELECT "people".* FROM "people"
 =>                                                           
[#<Person:0x00007fa187686bb0                                  
  id: 1,                                                      
  first_name: "Gon",                                          
  last_name: "Freaks",                                        
  phone: "619012345",                                         
  created_at: Thu, 17 Mar 2022 23:36:37.710193000 UTC +00:00, 
  updated_at: Thu, 17 Mar 2022 23:36:37.710193000 UTC +00:00>,
 #<Person:0x00007fa187686a70                                  
  id: 2,                                                      
  first_name: "Midoriya",                                     
  last_name: "Izuku",                                         
  phone: "8004156000",                                        
  created_at: Thu, 17 Mar 2022 23:39:01.596987000 UTC +00:00, 
  updated_at: Thu, 17 Mar 2022 23:39:01.596987000 UTC +00:00>,
 #<Person:0x00007fa1876869a8
  id: 3,
  first_name: "Hayao",
  last_name: "Miyazaki",
  phone: "81570055777",
  created_at: Thu, 17 Mar 2022 23:41:21.662260000 UTC +00:00,
  updated_at: Thu, 17 Mar 2022 23:41:21.662260000 UTC +00:00>,
 #<Person:0x00007fa1876868e0
  id: 4,
  first_name: "Borrito",
  last_name: "Uzumaki",
  phone: "50050005000",
  created_at: Thu, 17 Mar 2022 23:43:24.668747000 UTC +00:00,
  updated_at: Thu, 17 Mar 2022 23:43:24.668747000 UTC +00:00>,
 #<Person:0x00007fa187686818
  id: 5,
  first_name: "Ash",
  last_name: "Ketchum",
  phone: "000000000",
  created_at: Thu, 17 Mar 2022 23:44:03.661965000 UTC +00:00,
  updated_at: Thu, 17 Mar 2022 23:44:03.661965000 UTC +00:00>] 
3.0.0 :007 > 
^C
3.0.0 :007 > 
^C
3.0.0 :007 > 

3.0.0 :006 > Person.create first_name: "Naruto", last_name: "Uzumaki", phone: "4
088588855"
  TRANSACTION (3.5ms)  BEGIN
  Person Create (0.8ms)  INSERT INTO "people" ("first_name", "last_name", "phone", "created_at", "updated_at") VALUES ($1, $2, $3, $4, $5) RETURNING "id"  [["first_name", "Naruto"], ["last_name", "Uzumaki"], ["phone", "4088588855"], ["created_at", "2022-03-18 00:36:38.048861"], ["updated_at", "2022-03-18 00:36:38.048861"]]                                                                            
  TRANSACTION (3.0ms)  COMMIT                                                   
 =>                                                                             
#<Person:0x00007fe47a716518                                                     
 id: 6,                                                                         
 first_name: "Naruto",                                                          
 last_name: "Uzumaki",                                                          
 phone: "4088588855",                                                           
 created_at: Fri, 18 Mar 2022 00:36:38.048861000 UTC +00:00,                    
 updated_at: Fri, 18 Mar 2022 00:36:38.048861000 UTC +00:00> 
3.0.0 :007 > Person.all
  Person Load (2.2ms)  SELECT "people".* FROM "people"
 =>                                                           
[#<Person:0x00007fe47d639840                                  
  id: 1,                                                      
  first_name: "Gon",                                          
  last_name: "Freaks",                                        
  phone: "619012345",                                         
  created_at: Thu, 17 Mar 2022 23:36:37.710193000 UTC +00:00, 
  updated_at: Thu, 17 Mar 2022 23:36:37.710193000 UTC +00:00>,
 #<Person:0x00007fe47d639570                                  
  id: 2,                                                      
  first_name: "Midoriya",                                     
  last_name: "Izuku",                                         
  phone: "8004156000",                                        
  created_at: Thu, 17 Mar 2022 23:39:01.596987000 UTC +00:00, 
  updated_at: Thu, 17 Mar 2022 23:39:01.596987000 UTC +00:00>,
 #<Person:0x00007fe47a3381f8
  id: 3,
  first_name: "Hayao",
  last_name: "Miyazaki",
  phone: "81570055777",
  created_at: Thu, 17 Mar 2022 23:41:21.662260000 UTC +00:00,
  updated_at: Thu, 17 Mar 2022 23:41:21.662260000 UTC +00:00>,
 #<Person:0x00007fe47a32b868
  id: 4,
  first_name: "Borrito",
  last_name: "Uzumaki",
  phone: "50050005000",
  created_at: Thu, 17 Mar 2022 23:43:24.668747000 UTC +00:00,
  updated_at: Thu, 17 Mar 2022 23:43:24.668747000 UTC +00:00>,
 #<Person:0x00007fe47a32b0c0
  id: 5,
  first_name: "Ash",
  last_name: "Ketchum",
  phone: "000000000",
  created_at: Thu, 17 Mar 2022 23:44:03.661965000 UTC +00:00,
  updated_at: Thu, 17 Mar 2022 23:44:03.661965000 UTC +00:00>,
 #<Person:0x00007fe47a32af80
  id: 6,
  first_name: "Naruto",
  last_name: "Uzumaki",
  phone: "4088588855",
  created_at: Fri, 18 Mar 2022 00:36:38.048861000 UTC +00:00,
  updated_at: Fri, 18 Mar 2022 00:36:38.048861000 UTC +00:00>] 
3.0.0 :008 > Person.where last_name: "Uzumaki"
  Person Load (0.6ms)  SELECT "people".* FROM "people" WHERE "people"."last_name" = $1  [["last_name", "Uzumaki"]]                            
 =>                                                           
[#<Person:0x00007fe47d73f5a0                                  
  id: 4,                                                      
  first_name: "Borrito",                                      
  last_name: "Uzumaki",                                       
  phone: "50050005000",                                       
  created_at: Thu, 17 Mar 2022 23:43:24.668747000 UTC +00:00, 
  updated_at: Thu, 17 Mar 2022 23:43:24.668747000 UTC +00:00>,
 #<Person:0x00007fe47d73f4d8                                  
  id: 6,                                                      
  first_name: "Naruto",                                       
  last_name: "Uzumaki",                                       
  phone: "4088588855",                                        
  created_at: Fri, 18 Mar 2022 00:36:38.048861000 UTC +00:00,
  updated_at: Fri, 18 Mar 2022 00:36:38.048861000 UTC +00:00>] 
3.0.0 :009 > naruto = Person.find 6
  Person Load (0.6ms)  SELECT "people".* FROM "people" WHERE "people"."id" = $1 LIMIT $2  [["id", 6], ["LIMIT", 1]]                                    
 =>                                                                    
#<Person:0x00007fe47ea3a920                                            
...                                                                    
3.0.0 :010 > naruto.phone = "8589009000"
 => "8589009000" 
3.0.0 :011 > naruto.save
  TRANSACTION (0.3ms)  BEGIN
  Person Update (4.7ms)  UPDATE "people" SET "phone" = $1, "updated_at" = $2 WHERE "people"."id" = $3  [["phone", "8589009000"], ["updated_at", "2022-03-18 00:39:04.513620"], ["id", 6]]                                              
  TRANSACTION (0.9ms)  COMMIT                                          
 => true                                                               
3.0.0 :012 > Person.find 6
  Person Load (0.6ms)  SELECT "people".* FROM "people" WHERE "people"."id" = $1 LIMIT $2  [["id", 6], ["LIMIT", 1]]                           
 =>                                                           
#<Person:0x00007fe47a708a30                                   
 id: 6,                                                       
 first_name: "Naruto",                                        
 last_name: "Uzumaki",                                        
 phone: "8589009000",                                         
 created_at: Fri, 18 Mar 2022 00:36:38.048861000 UTC +00:00,  
 updated_at: Fri, 18 Mar 2022 00:39:04.513620000 UTC +00:00>  
3.0.0 :013 > Person.find(3).first_name
  Person Load (5.1ms)  SELECT "people".* FROM "people" WHERE "people"."id" = $1 LIMIT $2  [["id", 3], ["LIMIT", 1]]                                             
 => "Hayao"    