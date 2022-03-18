Challenges

# Set Up
- $ rails new favorite_movie -d postgresql -T
- $ cd favorite_band
- $ rails db:create
- $ rails server
### Created database 'favorite_movie_development'
### Created database 'favorite_movie_test'
- $ rails generate model Movie title:string category:string
- $ rails db:migrate
== 20220318205810 CreateMovies: migrating =====================================
-- create_table(:movies)
   -> 0.0308s
== 20220318205810 CreateMovies: migrated (0.0310s) ============================


- $ rails c



# Challenges

## Add five entries to the database via the Rails console
Movie.create title:"Fantastic Planet", category:"Sci-fi"
 Movie.create title:"School of Rock", category:"Comedy"
 Movie.create title:"Ponyo", category:"Fantasy"
 Movie.create title:"The Notebook", category:"Romance"
 Movie.create title:"Insidious", category:"Horror"

=>                                                          
[#<Movie:0x00007fc875523100                                  
  id: 1,                                                     
  title: "Fantastic Planet",                                 
  category: "Sci-fi",                                        
  created_at: Fri, 18 Mar 2022 18:19:55.407326000 UTC +00:00,
  updated_at: Fri, 18 Mar 2022 18:19:55.407326000 UTC +00:00>,
 #<Movie:0x00007fc875522f48                                  
  id: 2,                                                     
  title: "School of Rock",                                   
  category: "Comedy",                                        
  created_at: Fri, 18 Mar 2022 18:20:31.095353000 UTC +00:00,
  updated_at: Fri, 18 Mar 2022 18:20:31.095353000 UTC +00:00>,
 #<Movie:0x00007fc875522d90                                  
  id: 3,
  title: "Ponyo",
  category: "Fantasy",
  created_at: Fri, 18 Mar 2022 18:21:43.824108000 UTC +00:00,
  updated_at: Fri, 18 Mar 2022 18:21:43.824108000 UTC +00:00>,
 #<Movie:0x00007fc875522c50
  id: 4,
  title: "The Notebook",
  category: "Romance",
  created_at: Fri, 18 Mar 2022 18:22:13.845461000 UTC +00:00,
  updated_at: Fri, 18 Mar 2022 18:22:13.845461000 UTC +00:00>,
 #<Movie:0x00007fc875522b88
  id: 5,
  title: "Insidious",
  category: "Horror",
  created_at: Fri, 18 Mar 2022 18:22:53.195119000 UTC +00:00,
  updated_at: Fri, 18 Mar 2022 18:22:53.195119000 UTC +00:00>]

- $ Movie.all


Create a migration to add a new column to the database called movie_length
- $ rails generate migration add_column_movie_length
    - In the db/migrate def change 
    add_column :movies, :movie_length, :string
- $ rails db:migrate



Update the values of the five existing attributes to include a movie_length value
fantastic = Movie.find 1
fantastic.update movie_length:"1:00:00"
school = Movie.find 2
school.update movie_length:"1:00:00"
ponyo = Movie.find 3
ponyo.update movie_length:"1:00:00"
notebook = Movie.find 4
notebook.update movie_length:"1:00:00"
insidious = Movie.find 5
insidious.update movie_length:"1:00:00"


Generate a migration to rename the column 'category' to 'genre'
- $ rails generate migration change_name_of_category_to_genre

db/migrate
rename_column :movies, :category, :genre
- $ rails db:migrate





 =>                                                          
[#<Movie:0x00007fc228ca1380                                  
  id: 1,                                                     
  title: "Fantastic Planet",                                 
  genre: "Sci-fi",                                           
  created_at: Fri, 18 Mar 2022 20:59:39.913793000 UTC +00:00,
  updated_at: Fri, 18 Mar 2022 21:16:10.534302000 UTC +00:00,
  movie_length: "2:00:00">,                                  
 #<Movie:0x00007fc22c38e000                                  
  id: 2,                                                     
  title: "School of Rock",                                   
  genre: "Comedy",                                           
  created_at: Fri, 18 Mar 2022 21:00:16.288215000 UTC +00:00,
  updated_at: Fri, 18 Mar 2022 21:16:42.527046000 UTC +00:00,
  movie_length: "1:00:00">,
 #<Movie:0x00007fc22c38d970
  id: 3,
  title: "Ponyo",
  genre: "Fantasy",
  created_at: Fri, 18 Mar 2022 21:00:26.804150000 UTC +00:00,
  updated_at: Fri, 18 Mar 2022 21:17:21.366881000 UTC +00:00,
  movie_length: "1:00:00">,
 #<Movie:0x00007fc22c38d4c0
  id: 4,
  title: "The Notebook",
  genre: "Romance",
  created_at: Fri, 18 Mar 2022 21:00:46.073957000 UTC +00:00,
  updated_at: Fri, 18 Mar 2022 21:17:55.650673000 UTC +00:00,
  movie_length: "1:00:00">,
 #<Movie:0x00007fc22c38d038
  id: 5,
  title: "Insidious",
  genre: "Horror",
  created_at: Fri, 18 Mar 2022 21:00:54.635913000 UTC +00:00,
  updated_at: Fri, 18 Mar 2022 21:18:23.825353000 UTC +00:00,
  movie_length: "1:00:00">]

