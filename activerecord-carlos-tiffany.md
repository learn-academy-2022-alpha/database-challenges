As a developer, I have been tasked with creating a database model that will be used in a rolodex application. I want to ensure that the database behaves as expected and the necessary actions can be performed on the database instances.

Set Up

Create a new Rails app named 'rolodex_challenge'.
Create the database. The output in the terminal should look like this:
# Created database 'rolodex_development'
# Created database 'rolodex_test'
Generate a model called Person with a first_name, last_name, and phone. All fields should be strings.
$ rails generate model Person first_name:string last_name:string phone:string


Run a migration to set up the database.
$ rails db:migrate 

== 20220318000819 CreatePeople: migrating =====================================
-- create_table(:people)
   -> 0.0175s
== 20220318000819 CreatePeople: migrated (0.0176s) ============================


Open up Rails console.
$ rails c

Actions

Add five family members into the Person table in the Rails console.


Retrieve all the items in the database.
$ Person.all
 =>                                                           
[#<Person:0x00007fe204039bc8                                  
  id: 1,                                                      
  first_name: "Carlos",                                       
  last_name: "Ramos",                                         
  phone: "555-1211",                                          
  created_at: Fri, 18 Mar 2022 00:11:35.303512000 UTC +00:00, 
  updated_at: Fri, 18 Mar 2022 00:11:35.303512000 UTC +00:00>,
 #<Person:0x00007fe204039a88                                  
  id: 2,                                                      
  first_name: "Tiffany",                                      
  last_name: "Do",                                            
  phone: "4080651",                                           
  created_at: Fri, 18 Mar 2022 00:12:09.889200000 UTC +00:00, 
  updated_at: Fri, 18 Mar 2022 00:12:09.889200000 UTC +00:00>,
 #<Person:0x00007fe2040399c0
  id: 3,
  first_name: "Martina",
  last_name: "Ramos",
  phone: "555-1212",
  created_at: Fri, 18 Mar 2022 00:12:52.002205000 UTC +00:00,
  updated_at: Fri, 18 Mar 2022 00:12:52.002205000 UTC +00:00>,
 #<Person:0x00007fe2040398f8
  id: 4,
  first_name: "Tony",
  last_name: "Ramos",
  phone: "555-1213",
  created_at: Fri, 18 Mar 2022 00:13:14.784574000 UTC +00:00,
  updated_at: Fri, 18 Mar 2022 00:13:14.784574000 UTC +00:00>,
 #<Person:0x00007fe204039830
  id: 5,
  first_name: "Charles",
  last_name: "Do",
  phone: "408-0652",
  created_at: Fri, 18 Mar 2022 00:14:00.887528000 UTC +00:00,
  updated_at: Fri, 18 Mar 2022 00:14:00.887528000 UTC +00:00>] 



Add yourself to the Person table.



Retrieve all the entries that have the same last_name as you.
   $ Person.where last_name:"Do"
Person Load (0.9ms)  SELECT "people".* FROM "people" WHERE "people"."last_name" = $1  [["last_name", "Do"]]                   
 =>                                             
[#<Person:0x00007fe1fbd1ebf8                    
  id: 2,                                 
  first_name: "Tiffany",                 
  last_name: "Do",                       
  phone: "4080651",                      
  created_at: Fri, 18 Mar 2022 00:12:09.889200000 UTC +00:00,
  updated_at: Fri, 18 Mar 2022 00:12:09.889200000 UTC +00:00>,
 #<Person:0x00007fe1fbd1ea68             
  id: 5,                                 
  first_name: "Charles",                 
  last_name: "Do",                       
  phone: "408-0652",                     
  created_at: Fri, 18 Mar 2022 00:14:00.887528000 UTC +00:00,
  updated_at: Fri, 18 Mar 2022 00:14:00.887528000 UTC +00:00>] 



Update the phone number of the last entry in the database.

charles = Person.find 5
charles.phone = "555-1216"
charles.save

 #<Person:0x00007fe1ff22ae00
  id: 5,
  first_name: "Charles",
  last_name: "Do",
  phone: "555-1216",
  created_at: Fri, 18 Mar 2022 00:14:00.887528000 UTC +00:00,
  updated_at: Fri, 18 Mar 2022 00:16:56.861656000 UTC +00:00>] 

Retrieve the first_name of the third Person in the database.
thirdentry = Person.find 3
thirdentry.first_name
=> "Martina"



Stretch Challenges

Update all the family members with the same last_name as you, to have the same phone number as you.
Remove all family members that do not have your last_name.