Setup
Create a new rails application and database
- rails new associations_challenge -d postgresql -T
- cd associations_challenge
- rails db:create
- rails s


Create a model for owner
- rails generate model Owner name:string address:string num_credit:string
An owner has a name and address, and can have multiple credit cards

Create a model for credit card
- rails generate model Credit_Card number:string expdate:string owner_id:integer
A credit card has a number, an expiration date, and an owner


Challenges
Create three owners and save them in the database
- Owner.create name:"Michael", address:"420 High St", num_credit:"2"
- Owner.create name:"Tiffany", address:"123 Main St", num_credit:"1"
- Owner.create name:"Sam", address:"123 Sunset Blvd", num_credit:"1"


Create a credit card in the database for each owner
- credit_1 = Owner.find 1
- credit_1.credit_cards.create number:"1234567891", expdate:"03/22"

- credit_3 = Owner.find 3
- credit_3.credit_cards.create number:"1234567892", expdate:"05/27"

- credit_4 = Owner.find 2
- credit_4.credit_cards.create number:"0000000000", expdate:"05/26"

Add two more credit cards to one of the owners
- credit_2 = Owner.find 1
- credit_2.credit_cards.create number:"1234567890", expdate:"04/22"

- scredit_2 = Owner.find 1
credit_5.credit_cards.create number:"1000000000", expdate:"07/26"

numcredit_1 = Owner.find 1
numcredit_1.update num_credit:"3"


Owner.all
[#<Owner:0x00007f8341aa8e78                                           
  id: 2,                                                              
  name: "Tiffany",                                                    
  address: "123 Main St",                                             
  num_credit: "1",                                                    
  created_at: Mon, 21 Mar 2022 18:26:20.586124000 UTC +00:00,         
  updated_at: Mon, 21 Mar 2022 18:26:20.586124000 UTC +00:00>,
 #<Owner:0x00007f833ecc4de0                                  
  id: 3,                                                     
  name: "Sam",                                               
  address: "123 Sunset Blvd",                                
  num_credit: "1",                                           
  created_at: Mon, 21 Mar 2022 18:26:43.206778000 UTC +00:00,
  updated_at: Mon, 21 Mar 2022 18:26:43.206778000 UTC +00:00>,
 #<Owner:0x00007f833ecc4ca0
  id: 1,
  name: "Michael",
  address: "420 High St",
  num_credit: "3",
  created_at: Mon, 21 Mar 2022 18:23:08.543287000 UTC +00:00,
  updated_at: Mon, 21 Mar 2022 18:57:25.178929000 UTC +00:00>] 


Stretch Challenge
Add a credit limit to each card
rails g migration add_column_limit_to_credit 
=> db/migrate
structure: add_column :credit_cards, :limit, :integer
rails db:migrate 

limit1 = CreditCard.find 1
limit1.update limit:4000

limit2 = CreditCard.find 2
limit2.update limit:10000

limit3 = CreditCard.find 3
limit3.update limit:500

limit4 = CreditCard.find 4
limit4.update limit:50000

limit5 = CreditCard.find 5
limit5.update limit:1000

CreditCard.all


Find the total credit extended to the owner with multiple credit cards