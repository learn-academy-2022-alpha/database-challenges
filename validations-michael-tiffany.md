Validations Challenges
Create a Rails application called company_contacts. The app will have a PostgreSQL database.
Generate a model called Account that has a username, a password, and an email.
All stories should have accompanying model specs.
Developer Stories

As a developer, I need username, password, and email to be required.
As a developer, I need every username to be at least 5 characters long.
As a developer, I need each username to be unique.
As a developer, I need each password to be at least 6 characters long.
As a developer, I need each password to be unique.
As a developer, I want my Account model to have many associated Addresses.
As a developer, I want Address to have street_number, street_name, city, state, and zip attributes. The street_number and zip should be integers.
As a developer, I want to validate the presence of all fields on Address.

=> spec/models/account_spec.rb
require 'rails_helper'

RSpec.describe Account, type: :model do
  it 'valid with valid attributes' do
    tiffany = Account.create(username:'tiffanydoh', password:"abcdefg1", email:'tiffanydoh@gmail.com')
    expect(tiffany).to be_valid
  end
  it 'is not valid without an username' do
    tiffany = Account.create(password:"abcdefg1", email:'tiffanydoh@gmail.com')
    expect(tiffany.errors[:username]).to_not be_empty
  end
  it 'is not valid without a password' do
    tiffany = Account.create(username:"tiffanydoh", email:'tiffanydoh@gmail.com')
    expect(tiffany.errors[:password]).to_not be_empty
  end
  it 'is not valid without an email' do
    tiffany = Account.create(username:"tiffanydoh", password:"abcdefg1")
    expect(tiffany.errors[:email]).to_not be_empty
  end
  it 'username is not valid if its not at least 5 characters long' do
    tiffany = Account.create(username:'t', password:"abcdefg1", email:'tiffanydoh@gmail.com')
    expect(tiffany.errors[:username]).to_not be_empty
  end
  it 'username should be unique' do
    tiffany_valid = Account.create(username:'tiffanydoh', password:"abcdefg1", email:'tiffanydoh@gmail.com')
    tiffany_invalid = Account.create(username:'tiffanydoh', password:"abcdefg1", email:'tiffanydoh@gmail.com')
    expect(tiffany_invalid.errors[:username]).to_not be_empty
  end
  it 'password is not valid if its not at least 6 characters long' do
    tiffany = Account.create(username:'tiffanydoh', password:"a1", email:'tiffanydoh@gmail.com')
    expect(tiffany.errors[:password]).to_not be_empty
  end
  it 'password should be unique' do
    tiffany_valid = Account.create(username:'tiffanydoh', password:"abcdefg1", email:'tiffanydoh@gmail.com')
    tiffany_invalid = Account.create(username:'tiffanydoh', password:"abcdefg1", email:'tiffanydoh@gmail.com')
    expect(tiffany_invalid.errors[:password]).to_not be_empty
  end
  it 'each password should have at least one number' do
    tiffany = Account.create(username:'tiffanydoh', password:"abcdefg", email:'tiffanydoh@gmail.com')
    expect(tiffany.errors[:password]).to_not be_empty
  end
end

=> spec/models/address_spec.rb
require 'rails_helper'

RSpec.describe Address, type: :model do
  it 'valid with valid attributes' do
  tiffany_address = Address.create(street_number: 123, street_name: "Main St", city: "San Diego", state: "CA", zip:92105)
  expect(tiffany_address).to be_valid
  end
  it 'is not valid without a street number' do
    tiffany_address = Address.create(street_name: "Main St", city: "San Diego", state: "CA", zip:92105)
    expect(tiffany_address.errors[:street_number]).to_not be_empty
  end
  it 'is not valid without a street name' do
    tiffany_address = Address.create(street_number:123, city: "San Diego", state: "CA", zip:92105)
    expect(tiffany_address.errors[:street_name]).to_not be_empty
  end
  it 'is not valid without a city' do
    tiffany_address = Address.create(street_number:123, street_name: "Main St", state: "CA", zip:92105)
    expect(tiffany_address.errors[:city]).to_not be_empty
  end
  it 'is not valid without a state' do
    tiffany_address = Address.create(street_number:123, street_name: "Main St", city: "San Diego", zip:92105)
    expect(tiffany_address.errors[:state]).to_not be_empty
  end
  it 'is not valid without a zip' do
    tiffany_address = Address.create(street_number:123, street_name: "Main St", city: "San Diego", state:"CA")
    expect(tiffany_address.errors[:zip]).to_not be_empty
  end
end

=> app/models/account.rb

class Account < ApplicationRecord
    has_many :addresses

    validates :username, :password, :email, presence: true
    validates :username, length: { minimum: 5}
    validates :password, length: { minimum: 6}
    validates :username, :password, uniqueness: true
    
end

=> app/models/address.rb

class Address < ApplicationRecord
    belongs_to :account

    validates :street_number, :street_name, :city, :state, :zip, presence: true
end



Stretch Challenges

As a developer, I need each Account password to have at least one number.
HINT: Read about custom validations in the Active Record validation docs.
As a developer, I want to validate that Address street_number, street_name, zip are unique for within an account.
HINT: Read about :scope in the Active Record validation docs.
As a developer, I want to validate that the Address street_number and zip are numbers.
HINT: Read about numericality in the Active Record validation docs.
As a developer, I want to see a custom error message that says "Please, input numbers only" if street_number or zip code are not numbers.
HINT: Read about message in the validation docs.
