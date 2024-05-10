# LightBnB

## Project Structure

```
.
├── db
│   ├── json
│   └── database.js
├── public
│   ├── javascript
│   │   ├── components
│   │   │   ├── header.js
│   │   │   ├── login_form.js
│   │   │   ├── new_property_form.js
│   │   │   ├── property_listing.js
│   │   │   ├── property_listings.js
│   │   │   ├── search_form.js
│   │   │   └── signup_form.js
│   │   ├── libraries
│   │   ├── index.js
│   │   ├── network.js
│   │   └── views_manager.js
│   ├── styles
│   │   ├── main.css
│   │   └── main.css.map
│   └── index.html
├── routes
│   ├── apiRoutes.js
│   └── userRoutes.js
├── styles
│   ├── _forms.scss
│   ├── _header.scss
│   ├── _property-listings.scss
│   └── main.scss
├── .gitignore
├── package-lock.json
├── package.json
├── README.md
└── server.js
```

-   `db` contains all the database interaction code.
    -   `json` is a directory that contains a bunch of dummy data in `.json` files.
    -   `database.js` is responsible for all queries to the database. It doesn't currently connect to any database, all it does is return data from `.json` files.
-   `public` contains all of the HTML, CSS, and client side JavaScript.
    -   `index.html` is the entry point to the application. It's the only html page because this is a single page application.
    -   `javascript` contains all of the client side javascript files.
        -   `index.js` starts up the application by rendering the listings.
        -   `network.js` manages all ajax requests to the server.
        -   `views_manager.js` manages which components appear on screen.
        -   `components` contains all of the individual html components. They are all created using jQuery.
-   `routes` contains the router files which are responsible for any HTTP requests to `/users/something` or `/api/something`.
-   `styles` contains all of the sass files.
-   `server.js` is the entry point to the application. This connects the routes to the database.

LightBnB
Welcome to LightBnB, a simplified version of Airbnb for booking accommodations. This app allows users to browse listings, view details of properties, make bookings, and leave reviews.

Features
User Authentication: Users can sign up, log in, and log out securely.
Browse Listings: Users can view available listings with details such as title, description, price, and average rating.
Search Functionality: Users can search for listings based on various criteria such as location, price range, and minimum rating.
View Property Details: Users can view detailed information about each property including amenities, number of bedrooms and bathrooms, and host information.
Bookings: Users can make bookings for selected properties based on their desired dates and number of guests.
Reviews: Users can leave reviews and ratings for properties they have booked.

Technologies Used
Frontend:
HTML, CSS, JavaScript

Backend:
Node.js with Express.js for building RESTful APIs
PostgreSQL as the relational database management system

Getting Started
To run the LightBnB app locally, follow these steps:

Clone the repository: git clone git@github.com:dcminogue/LightBnB.git

Navigate to the project directory: cd LightBnB

Install dependencies: npm install

Set up the database:
Create a PostgreSQL database named lightbnb.
Run the SQL scripts in the database directory to create tables and seed data.

Run the server: npm run local

Access the application in your browser: http://localhost:3000

Screenshots:

![Home Page](../images/LightBnB-Home.png)
![Create Listing](../images/LightBnB-CreateListing.png)
![Database](../images/LightBnB-Database.png)
