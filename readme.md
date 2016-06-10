#Bodyshop Part 2

Cars are great and all, but now it's time to extend this system and make it handle more types of vehicles.

Remember TDD? This time, you'll have to make your own tests for each feature. In many work environments, **you** will be the one writing tests. As a reminder, here's the workflow:

1. Read each feature below and think about what it's asking for.
2. Create a test (in test.js) to test the feature
3. Run the test
4. Write / revise code (in Motorcycle.js/Truck.js) to pass test, if necessary
5. Repeat 3 and 4 until you pass all tests
6. Move on to the next feature (start back at step 1)

##Getting Started

* Fork and clone the repository
* Run `npm install` to install dependencies
  * `npm run lint:js` - lint JS
  * `npm test` - run test suite

## Writing Tests

In order to write tests, it's recommended that you look back at the tests for `Car.js` and start following some of the examples in order to get a feel for how to structure tests. Take advantage of the following functions:

* `assert.strictEqual(val1, val2, 'msg')` - strictly compares two primitive values
* `assert.deepEqual(val1, val2, 'msg')` - strictly compares the properties of two objects or arrays
* `instanceof` - compares an object and a constructor, and sees if the object is an instance of the constructor
* `success()` - a helper method defined in `test/helpers/success.js` that provided a success message after test units

## Requirements

###Pair Programming

For more real-world TDD experience, you'll pair up with a partner and practice pair programming, a technique used by companies such as Pivotal Labs. When pair programming, one person will act as the "driver", writing the code, while the other person acts as the "navigator", reviewing the code. Switch off every 10 minutes. Once finished, each person should make their own separate pull request and make a note of their partner in the pull request notes.

###Part 1 -- Trucks

Create a new constructor called `Truck` that extends `Car`.

This should be done in the file called `Truck.js`, which requires `Car.js` for you to use. Additionally your `truckTest.js` will need to require `Truck.js` (already done for you).

Your `Truck` constructor should meet the following requirements. There should be at least one test for each bullet point below.

* Must be an instance of `Truck`
* Must be an instance of `Car`.
* Must have the following constructor parameters:
  * make (string)
  * model (string)
  * year (number)
  * color (string)
  * cargoInPounds (number)
  * passengers (optional array)
* Must default to 3 seats.

There should be tests for each one of the bullet points above.

###Part 2 -- Motorcycles

Create a new constructor called `Motorcycle` that inherits your `Car` constructor.

This should be done in the file called `Motorcycle.js`, which requires `Car.js` for you to use. Additionally your `motorcycleTest.js` will need to require `Motorcycle.js` (already done for you).

Your `Motorcycle` constructor should meet the following requirements. There should be at least one test for each bullet point below.

* Must be an instance of a `Motorcycle`
* Must be an instance of a `Car`
* Must have the following parameters
  * make
  * model
  * year
  * color
  * seats
  * passengers
* Must default to 2 seats
* Must be able to do a wheelie by calling `wheelie()`, but only if running.
  * If the wheelie is successful, return true and `console.log` the following: `"Doing a sick wheelie!!"`. Otherwise return false.
  * This function should be attached to `Car.prototype`.
