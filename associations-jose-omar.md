rails new cards -d postgresql -T

 cd cards

 rails db:create

 rails s

rails g model Owner name:string address:string cards:integer
create    db/migrate/20220321175532_create_owners.rb
create    app/models/owner.rb


rails g model Owner name:string address:string cards:integer

rails g model Credit_card number:integer expiration:string owner_id:integer

rails db:migrate

rails c

 Owner.create name:"Omar", address:"123 Bronx St.", cards:1
 Owner.create name:"Jose", address:"123 Grape St.", cards:2
 Owner.create name:"Jacob", address:"435 Street Ln.", cards:5


 class Owner < ApplicationRecord
    has_many :credit_card
end


class CreditCard < ApplicationRecord
    belongs_to :owner
end


rails db:migrate


omar = Owner.find 1
omar.credit_card.create number:123456, expiration:"01/02"
 id: 1,
 number: 123456,
 expiration: "01/02",
 owner_id: 1,

jose = Owner.find 2
jose.credit_card.create number:456789, expiration:"05/22"
 id: 2,                                                                         
 number: 456789,                                                                
 expiration: "05/22",                                                           
 owner_id: 2,  


jacob = Owner.find 3
jacob.credit_card.create number:134569, expiration:"10/25"
 id: 3,                                                                         
 number: 134569,                                                                
 expiration: "10/25",                                                           
 owner_id: 3,  


 omar.credit_card.create number:555666, expiration:"12/30"
 omar.credit_card.create number:666433, expiration:"2/24"

  id: 4,                                                                         
 number: 555666,                                                                
 expiration: "12/30",                                                           
 owner_id: 1, 

  id: 5,
 number: 666433,
 expiration: "2/24",
 owner_id: 1,



 rails g migration card_limit

 class CardLimit < ActiveRecord::Migration[7.0]
  def change
    add_column :credit_cards, :credit_limit, :integer
  end
end


rails db:migrate

rails c
omar = CreditCard.find 1
omar.update credit_limit:1000

jose = CreditCard.find 2
jose.update credit_limit:1000

jacob = CreditCard.find 3
jacob.update credit_limit:5000

four = CreditCard.find 4
four.update credit_limit:5000


five = CreditCard.find 5
five.update credit_limit:10000
