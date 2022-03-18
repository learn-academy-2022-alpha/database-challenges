<!-- Favorite Movies Challenge
Create a new Rails application called 'favorite_movies'.
Create the database
Generate a Movie model with a title attribute and a category attribute
Challenges
Add five entries to the database via the Rails console
Create a migration to add a new column to the database called movie_length
Update the values of the five existing attributes to include a movie_length value
Generate a migration to rename the column 'category' to 'genre' -->



rails new favorite_movies -d postgresql -T

cd favorite_movies

$ rails db:create
Created database 'favorite_movies_development'
Created database 'favorite_movies_test'

rails s
http://localhost:3000/

rails generate model Movie title:string category:string
 create    db/migrate/20220318174900_create_movies.rb
      create    app/models/movie.rb


rails db:migrate

Movie.create title: "Coach Carter", category: "Sports"
Movie.all

rails generate migration add_movie_length
      create    db/migrate/20220318175837_add_movie_length.rb




class AddMovieLength < ActiveRecord::Migration[7.0]
  def change
    add_column :movies, :movie_length, :string
  end
end


rails db:migrate

turningred = Movie.find(1)
turningred.update movie_length:100

[#<Movie:0x00007fc33d80f798                                  
  id: 1,                                                     
  title: "Turning Red",                                      
  category: "Family",                                        
  created_at: Fri, 18 Mar 2022 17:55:02.164834000 UTC +00:00,
  updated_at: Fri, 18 Mar 2022 18:13:54.784435000 UTC +00:00,
  movie_length: 100>,                                        
 #<Movie:0x00007fc33d80f6d0                                  
  id: 2,                                                     
  title: "Training Day",                                     
  category: "Action",                                        
  created_at: Fri, 18 Mar 2022 17:55:30.181045000 UTC +00:00,
  updated_at: Fri, 18 Mar 2022 18:14:53.564441000 UTC +00:00,
  movie_length: 122>,
 #<Movie:0x00007fc33d80f608
  id: 3,
  title: "Shang-Chi",
  category: "Action",
  created_at: Fri, 18 Mar 2022 17:56:04.109903000 UTC +00:00,
  updated_at: Fri, 18 Mar 2022 18:15:37.949954000 UTC +00:00,
  movie_length: 132>,
 #<Movie:0x00007fc33d80f540
  id: 4,
  title: "Coach Carter",
  category: "Sports",
  created_at: Fri, 18 Mar 2022 17:56:22.022658000 UTC +00:00,
  updated_at: Fri, 18 Mar 2022 18:16:15.704118000 UTC +00:00,
  movie_length: 136>,
 #<Movie:0x00007fc33d80f478
  id: 5,
  title: "Hot Fuzz",
  category: "Comedy",
  created_at: Fri, 18 Mar 2022 17:56:51.260618000 UTC +00:00,
  updated_at: Fri, 18 Mar 2022 18:16:44.764232000 UTC +00:00,
  movie_length: 121>] 


rails generate migration change_category_name
create    db/migrate/20220318181908_change_category_name.rb


class ChangeCategoryName < ActiveRecord::Migration[7.0]
  def change
    rename_column :movies, :category, :genre
  end
end

