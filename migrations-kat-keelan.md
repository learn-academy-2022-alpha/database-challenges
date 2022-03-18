rails generate model Movie title:string category:string

3.0.0 :002 > Movie.create name: "Django", category: "Action"
3.0.0 :004 > Movie.create title: "Encanto", category: "Family"
3.0.0 :005 > Movie.create title: "The Emperor's New Groove", category: "Family"
3.0.0 :006 > Movie.create title: "Shaun of the Dead", category: "Comedy"
3.0.0 :007 > Movie.create title: "The Shinning", category: "Thriller"




3.0.0 :011 > add_column :list, :movie_length, :string


learnacademy@LEARNs-Air-3 favorite_movies % rails generate migration add_columns_to_movie movie_length:string       
      invoke  active_record
      create    db/migrate/20220318184319_add_columns_to_movie.rb
learnacademy@LEARNs-Air-3 favorite_movies % rails db:migrate
== 20220318184319 AddColumnsToMovie: migrating ================================
-- add_column(:movies, :movie_length, :string)
rails aborted!
StandardError: An error has occurred, this and all later migrations canceled:

PG::DuplicateColumn: ERROR:  column "movie_length" of relation "movies" already exists
/Users/learnacademy/Desktop/database-challenges/favorite_movies/db/migrate/20220318184319_add_columns_to_movie.rb:3:in `change'

Caused by:
ActiveRecord::StatementInvalid: PG::DuplicateColumn: ERROR:  column "movie_length" of relation "movies" already exists
/Users/learnacademy/Desktop/database-challenges/favorite_movies/db/migrate/20220318184319_add_columns_to_movie.rb:3:in `change'

Caused by:
PG::DuplicateColumn: ERROR:  column "movie_length" of relation "movies" already exists
/Users/learnacademy/Desktop/database-challenges/favorite_movies/db/migrate/20220318184319_add_columns_to_movie.rb:3:in `change'
Tasks: TOP => db:migrate
(See full trace by running task with --trace)
learnacademy@LEARNs-Air-3 favorite_movies % 
