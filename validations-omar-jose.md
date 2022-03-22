// rails set up commands
// rails bundle add rspec-rails
// rails generate rspec:install
// rails generate model Account username:string password:string email:string

//rails db:migrate
//models--->account_spec.rb
line 4:
    it 'valid with valid attributes' do
    user1= Account.create(username: 'Omar', password: 'abcd', email: 'omarbowen24@gmail.com')
    expect(user1).to be_valid
end
end

//app---models---account.rb
line 2:
validates :username, :password, :email, presence: true

//in terminal : rspec spec/models/account_spec.rb

'Finished in 0.15527 seconds (files took 6.71 seconds to load)
1 example, 0 failures'

//models--->account_spec.rb
add text below on line 8:
  user1= Account.create(username: 'O', password: 'abcd', email: 'omarbowen24@gmail.com')
  expect(user1.errors[:username]).to_not be_empty
end
end

//app ---models -- account.rb
ADD this on line 3
validates :username, length: { minimum: 5 }

//models---account_spec.rb
add on line 12

it 'each name should be unique' do
  user1_valid= Account.create(username: 'Omar Bowen', password: 'abcd', email: 'omarbowen24@gmail.com')
  user1_invalid= Account.create(username: 'Omar Bowen', password: 'abcd', email: 'omarbowen24@gmail.com')
  expect(user1_invalid.errors[:username]).to_not be_empty
  end
end

//app---models---account.rb
add on line 4
  validates :username, uniqueness: true

accout_spec.rb
add on line 17
it 'password is not valid if less than six characters' do
  user1= Account.create(username: 'Omar Bowen', password: 'abcd', email: 'omarbowen24@gmail.com')
  expect(user1.errors[:password]).to_not be_empty

//app---models---account.rb
add  on line 5
validates :password, length: { minimum: 6 }

account_spec.rb
it 'each password should be unique' do
  user1_valid= Account.create(username: 'Omar Bowen', password: 'abcdef', email: 'omarbowen24@gmail.com')
  user1_invalid= Account.create(username: 'Omar Bowen', password: 'abcdef', email: 'omarbowen24@gmail.com')
  expect(user1_invalid.errors[:password]).to_not be_empty
end

//app---models---account.rb
add on next line
validates :password, uniqueness: true

//add in terminal
rails g model Addresses street_number:integer street_name:string city:string state:string zip:integer account_id:integer

// in account.rb
add on line 7 has_many :addresses

// in address.rb
add on line 2
belongs_to :account
  validates :street_number, :street_name, :city, :state, :zip, presence: true

// in address_spec.rb
on line 4 add
it 'valid with valid attributes' do
    address1= Address.create(street_number: 123, street_name: "Grape Street", city: "San Diego", state: "CA", zip: 92029)
    expect(address1).to be_valid
