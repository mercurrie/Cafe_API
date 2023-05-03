# Cafe_API
Custom built API using RESTful Routing

Documentation 
https://documenter.getpostman.com/view/27214570/2s93eU4abR

This is a Flask web application that provides a RESTful API for a database of cafes. The API allows users to search for cafes by location, get a random cafe, add a new cafe, update a cafe's coffee price, and delete a cafe. The cafes are represented by a Cafe class in Python, and are stored in a SQLite database using SQLAlchemy.

Requirements
To run this application, you need to have Python 3 installed, as well as the following packages:

Flask
Flask-SQLAlchemy
You can install these packages using pip:

Copy code: pip install Flask Flask-SQLAlchemy

Usage
To run the application, execute the app.py script:

Copy code: python app.py
This will start the Flask development server and make the API available at http://localhost:5000/.

API Routes
GET /: returns the homepage of the web application
GET /all: returns all the cafes in the database
GET /random: returns a random cafe from the database
GET /search?loc=<location>: returns the cafe at the specified location
GET /update-price/<cafe_id>?new_price=<new_price>: updates the coffee price of the cafe with the given ID
POST /add: adds a new cafe to the database
DELETE /report-closed/<cafe_id>?api-key=<api_key>: deletes the cafe with the given ID, if the correct API key is provided
Authentication
To delete a cafe, you need to provide an API key as a query parameter in the URL. The API key is currently set to "TopSecretAPIKey" in the code, but you can change it to a more secure value.

Data Model
The Cafe class represents the cafes in the database. It has the following attributes:

id: an integer ID that uniquely identifies the cafe
name: a string that represents the name of the cafe
map_url: a string that represents the URL of the cafe's location on Google Maps
img_url: a string that represents the URL of the cafe's image
location: a string that represents the location of the cafe
seats: a string that represents the number of seats in the cafe
has_toilet: a boolean that indicates whether the cafe has a toilet
has_wifi: a boolean that indicates whether the cafe has wifi
has_sockets: a boolean that indicates whether the cafe has power sockets
can_take_calls: a boolean that indicates whether the cafe can take phone calls
coffee_price: a string that represents the price of the cafe's coffee
