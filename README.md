# README
Story 1: In order to track wildlife sightings, as a user of the API, I need to manage animals.

Branch: animal-crud-actions

Acceptance Criteria

Create a resource for animal with the following information: common name and scientific binomial✅

$ rails generate resource Animal common_name:string scientific_binomial:string
in console create some animals
Disabling authenticity token #skip_before_action :verify_authenticity_token to application controller 
start the server

IN controller.rb ---> add index 
also add 
private
    def animal_params
        params.require(:animal).permit(:common_name,:scientific_binomial)
    end

Can see the data response of all the animals✅
IN controller.rb ---> add show

Can create a new animal in the database✅
IN controller.rb ----> add create

Can update an existing animal in the database✅
IN controller.rb ---> add update

Can remove an animal entry in the database✅
IN controller.rb ----> add destroy




This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
