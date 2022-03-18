Favorite Movies Challenge

Setup
Create a new Rails application called 'favorite_movies'.

$rails new favorite_movies -d postgresql -- [ ]

Create the database

cd favorite_movies
$rails db:create

Generate a Movie model with a title attribute and a category attribute

$rails generate model Movie title:string category:string

Challenges
Add five entries to the database via the Rails console

$rails console
Movie.create title:"The Dark Knight", category:"Crime Thriller"
Movie.create title:"Airplane!", category:"Comedy"
Movie.create title:"Toy Story", category:"Animation"
Movie.create title:"Uncharted", category:"Action"
Movie.create title:"Midsommar", category:"Horror"

Create a migration to add a new column to the database called movie_length

$rails generate migration add_movie_length_to_movie

add_column :movies, :movie_length, :string

$rails db:migrate

Update the values of the five existing attributes to include a movie_length value
dark_knight = Movie.find 1
dark_knight.update movie_length:"145min"

airplane = Movie.find 2
airplane.update movie_length:"90min"

toy_story = Movie.find 3
toy_story.update movie_length:"95min"

uncharted = Movie.find 4
uncharted.update movie_length:"120min"

midsommar = Movie.find 5
midsommar.update movie_length:"130min"


Generate a migration to rename the column 'category' to 'genre'

$rails generate migration change_category_to_genre
$rails db:migrate

rename_column :movies, :category, :genre
