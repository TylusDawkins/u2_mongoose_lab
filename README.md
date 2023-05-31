

# Mongoose Flights Lab

## Intro

For this lab, lets create a database of Flights and use a model of Flights and Airports.

You'll begin by creating a `mongoose-flights` project using our usual commands (feel free to reference previous lessons for this!)
```sh
npm init -y
npm i mongoose
```

What folders and files we will we need to create as well?

## Exercises

1) Populate your **db/index.js** file that connects to a database.


2) Create a Model of Airport with the following properties:

	| Property | Type |
	|---|---|
	| `name`| `String`|  (Logan, LaGuardia, Heathrow, O'Hare, Pearson...)
	| `location`| `String`| (Boston, New York, London, Chicago, Toronto...)
	| `code`| `String`|    (LGN, LGA, HRT, OHR, YYZ...)



3) Create a `Flight` Model with the following properties, making sure its linked to the respective airports they'll be flying in and out of:

	| Property | Type |
	|---|---|
	| `airline`| `String`| ('American', 'Southwest', 'Delta'...)
	 |`flight number` |`Integer`| 
	 |`price`|`float`| 
	 |`numberOfSeats`|`integer`|
	 |`departingAirport`| `ref - airport_id`| 
	 |`arrivalAirport`|`ref - airport_id`| 
	 |`departure date/time` | Your choice! How do you think we should add this in? |
	 
	 
	 Which of our models is the Parent, which is the Child? How are we connecting the two?

4. Seed your db with at least 4 airports and at least 7 flights. Use your Mongo shell, or your query.js file to Read all of your data before working with the features in the following prompt. 

5. Implement the following features:
	- A User, should be able to view a list of all flights and airports (`index` functionality) that displays each flight's airline, airport, flight no., and departure date/time (consider formatting the `departs` property).
	
	- A User should be able to access the details for each of these objects via a Show route based on the object's ID

	- A User should be able to create flights by entering the information for Airports and Flights using a Query.js file that you will create
	
	- A User should be able to update the details for my Flights and Airports
	
	- A User should be able to delete any Flight and Airport
	

#### Hints:

- Checkout the [Date datatype 
](https://www.mongodb.com/docs/manual/reference/method/Date/) to assist users in entering valid date/time values.

## Bonuses


1. Code these additional features:
	- A User should be able to view the list of flights by departure date in ascending order.
	
	- The flights in the should not be displayed if the flight's departure date and time have passed.

	- A User should be able to see all flights from California to New York by descending price (hint - you may need to create a number of Flight objects that meet this requirement. You can use JFK and LGA for New York airports, and LAX and SFO for California's)

