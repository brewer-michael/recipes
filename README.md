# README

* Add a scaffolded item (Example from https://www.digitalocean.com/community/tutorials/how-to-build-a-ruby-on-rails-application)

$ rails generate scaffold Shark name:string facts:text

Edit config/routes.rb

Add ```root 'sharks#index'``` and save the file

Run $ rails db:migrate

Run server $ rails server -p $PORT -b 0.0.0.0

* Add Validations
Edit app/models/shark.rb

Add lines to validate fields and make sure Name is distinct
##```validates :name, presence: true, uniqueness: true
validates :facts, presence: true```##

* Placeholder
Add authenticated user to application controller

Edit app/controllers/application_controller.rb
##```http_basic_authenticate_with name: 'sammy', password: 'shark', except: [:index, :show]```##

* ...
