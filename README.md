# Cafe_API
Custom built API using RESTful Routing

Documentation 
https://documenter.getpostman.com/view/27214570/2s93eU4abR

# Flask Cafe API

This is a Flask-based API that manages a database of cafes, allowing users to perform various CRUD operations through RESTful routing. The app uses SQLite as the database backend and SQLAlchemy as the ORM.

## Requirements

- Flask==2.0.1
- Flask_SQLAlchemy==2.5.1

## Installation

1. Clone the repository
2. Install the requirements with `pip install -r requirements.txt`
3. Run the app with `python app.py`

## Routes

- `GET /` - displays the index page
- `GET /random` - returns a random cafe from the database
- `GET /all` - returns a list of all cafes in the database
- `GET /search?loc=<location>` - returns a cafe with the specified location
- `POST /add` - adds a new cafe to the database
- `PATCH /update-price/<int:cafe_id>` - updates the price of a cafe with the specified ID
- `DELETE /report-closed/<int:cafe_id>?api-key=<api_key>` - deletes a cafe with the specified ID, if the correct API key is provided

## Contributing

Contributions are welcome! If you would like to contribute to this project, please fork the repository and submit a pull request.

## License

This project is licensed under the [MIT License](https://github.com/yourusername/flask-cafe-api/blob/main/LICENSE).
Remember to replace yourusername in the license section with your GitHub username.






