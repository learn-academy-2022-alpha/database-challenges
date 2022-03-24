Validations Challenges
Create a Rails application called company_contacts. The app will have a PostgreSQL database.

$ rails new company-contacts -d postgresql
$ cd company-contacts
$ rails db:create
$ bundle add rspec-rails
$ rails generate rspec:install

Generate a model called Account that has a username, a password, and an email.

$ rails generate model Account username:string password:string email:string
$ rails db:migrate
$ rails server

All stories should have accompanying model specs.

Developer Stories

As a developer, I need username, password, and email to be required.

RSpec.describe Account, type: :model do
  it 'valid with valid entries' do
    carlos = Account.create password:"peanutbutter", email:"pb@gmail.com"
    expect(carlos.errors[:username]).to_not be_empty
  end
  it 'is not valid without a password' do
    carlos = Account.create username:"caramos", email:"pb@gmail.com"
    expect(carlos.errors[:password]).to_not be_empty
  end
  it 'is not valid without an email' do
    carlos = Account.create username:"caramos", password:"peanutbutter"
    expect(carlos.errors[:email]).to_not be_empty
  end
end

validates :username, :password, :email, presence: true

As a developer, I need every username to be at least 5 characters long.

it 'username is not valid if less than 5 characters' do
  carlos = Account.create username:"car", password:"peanutbutter", email:"pb@gmail.com"
  expect(carlos.errors[:username]).to_not be_empty
end

validates :username, length: { minimum: 5 }

As a developer, I need each username to be unique.

it 'each username should be unique' do
    carlos_valid = Account.create username:"caramos", password:"peanutbutter", email:"pb@gmail.com"
    carlos_invalid = Account.create username:"caramos", password:"peanutbutter", email:"pb@gmail.com"
    expect(carlos_invalid.errors[:username]).to_not be_empty
end

validates :username, uniqueness: true

As a developer, I need each password to be at least 6 characters long.

it 'password is not valid if less than 6 characters' do
  carlos = Account.create username:"caramos", password:"pea", email:"pb@gmail.com"
  expect(carlos.errors[:password]).to_not be_empty
end

validates :password, length: { minimum: 6 }


As a developer, I need each password to be unique.

it 'each password should be unique' do
    carlos_valid = Account.create username:"caramos", password:"peanutbutter", email:"pb@gmail.com"
    carlos_invalid = Account.create username:"caramos", password:"peanutbutter", email:"pb@gmail.com"
    expect(carlos_invalid.errors[:password]).to_not be_empty
end

validates :password, uniqueness: true


As a developer, I want my Account model to have many associated Addresses.

As a developer, I want Address to have street_number, street_name, city, state, and zip attributes. The street_number and zip should be integers.

$ rails generate model Address street_number:integer street_name:string city:string state:string zip:integer
$ rails db:migrate

class Account < ApplicationRecord
  has_many :addresses
end

class Address < ApplicationRecord
  belongs_to :account
end

As a developer, I want to validate the presence of all fields on Address.

it 'is not valid without a street number' do
    carlos = Address.create street_name:"elm street", city:"San Diego", state:"CA", zip:92017
    expect(carlos.errors[:street_number]).to_not be_empty
end

validates :street_number, presence: true

it 'is not valid without a street name' do
    carlos = Address.create street_number: 2352, city:"San Diego", state:"CA", zip:92017
    expect(carlos.errors[:street_name]).to_not be_empty
end

validates :street_number, :street_name, presence: true

it 'is not valid without a city' do
    carlos = Address.create street_number: 2352, street_name:"elm street", state:"CA", zip:92017
    expect(carlos.errors[:city]).to_not be_empty
end

validates :street_number, :street_name, :city, presence: true

it 'is not valid without a state' do
    carlos = Address.create street_number: 2352, street_name:"elm street", city:"San Diego", zip:92017
    expect(carlos.errors[:state]).to_not be_empty
end

validates :street_number, :street_name, :city, :state, presence: true

it 'is not valid without a zip' do
    carlos = Address.create street_number: 2352, street_name:"elm street", city:"San Diego", state:"CA"
    expect(carlos.errors[:zip]).to_not be_empty
end

validates :street_number, :street_name, :city, :state, :zip, presence: true

Stretch Challenges

As a developer, I need each Account password to have at least one number.

HINT: Read about custom validations in the Active Record validation docs.

As a developer, I want to validate that Address street_number, street_name, zip are unique for within an account.


HINT: Read about :scope in the Active Record validation docs.

As a developer, I want to validate that the Address street_number and zip are numbers.

HINT: Read about numericality in the Active Record validation docs.

it 'street number should only be a number' do
    carlos = Address.create street_number:"hello", street_name:"elm street", city:"San Diego", state:"CA", zip:92017
    expect(carlos.errors[:street_number]).to_not be_empty
end

validates :street_number, numericality: { only_integer: true }

it 'zip should only be a number' do
    carlos = Address.create street_number: 2352, street_name:"elm street", city:"San Diego", state:"CA", zip:"hello"
    expect(carlos.errors[:zip]).to_not be_empty
end

validates :street_number, :zip, numericality: { only_integer: true }

As a developer, I want to see a custom error message that says "Please, input numbers only" if street_number or zip code are not numbers.

HINT: Read about message in the validation docs.

validates :street_number, :zip, numericality: { only_integer: true, message:"Please input numbers only." }
