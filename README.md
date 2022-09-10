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
also add at the end but within 
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


Story 2: In order to track wildlife sightings, as a user of the API, I need to manage animal sightings.

Branch: sighting-crud-actions

Acceptance Criteria

Create a resource for animal sightings with the following information: latitude, longitude, date✅

Hint: An animal has_many sightings (rails g resource Sighting animal_id:integer ...)
Hint: Date is written in Active Record as yyyy-mm-dd (“2022-07-28")

generate a migrate ---> $rails generate migration sighting_migrate
$ rails generate resource Sighting animal_id:integer latitude:string longitude:string date:date

IN sightings_controller.rb ---> add index and show

Can create a new animal sighting in the database✅
IN sightings_ontroller.rb ---> add create

Can update an existing animal sighting in the database✅
IN sightings_ontroller.rb ---> add update

Can remove an animal sighting in the database✅
IN sightings_ontroller.rb ---> add destroy


