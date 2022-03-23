$ rails new routes_controllers_views_params -d postgresql -T
$ cd routes_controllers_views_params
Create a database: $ rails db:create
Begin the rails server: $ rails server
In a browser navigate to: http://localhost:3000


rails generate controller Main
  create  app/controllers/main_controller.rb
      invoke  erb
      create    app/views/main
      invoke  helper
      create    app/helpers/main_helper.rb


created team.html.erb
root 'main#team'

created jose.html.erb, kendra.html.erb, kat.html.erb files in views

inside team.html.erb
<h1> team members</h1>
<%= link_to 'jose', '/jose'%>
<%= link_to 'kendra', '/kendra'%>
<%= link_to 'kat', '/kat'%>


