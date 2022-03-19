//steps
// cd Desktop
// Rails new favorite_movies -d postgresql -T
// cd into directory: cd favorite_movies (cd file_name)
//Rails db:create
// rails s
// enter http://localhost:3000 into browser

// in new terminal tab cd into the database-challenges repo
// open up the text editor and save a .md file with the steps of all your work
//you can close this terminal tab when you're done

//run rails c in terminal (this starts the rails process)
//rails generate model favorite_movies title:string category:string
//open up text editor and it shoulder have the model with documents in it (remember all commands need to have rails c first)


// Movie.create title: "Titanic", category: "Drama"
// Movie.create title: "White chicks", category: "comedy"
// Movie.create title: "Remember the Titans", category: "Sports"
// Movie.create title: "Jaws", category: "Scary"
// Movie.create title: "Hangover", category: "comedy"

//rails generate migration add_movie_length
//rails db:migrate
//rails z
//Movie.all (see all the movies we made

//titanic= Movie.find 1
//titanic.update movie_length: 194
//remember_the_titans= Movie.find 3
//remember_the_titans.update movie_length: 113
//white_chicks= Movie.find 2
//white_chicks.update movie_length: 109
//jaws= Movie.find 4
//jaws.update movie_length: 124
//Hangover= Movie.find 5
//titanic.update movie_length: 140

//Movie all
//exit

//in the add_movie_length file under migrate in the text editor add "add_column :movies, :movie_length, :integer" in the line under def change 
