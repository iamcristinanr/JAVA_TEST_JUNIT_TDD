# Implementing TEST with JUNIT and mockito in Movies App.

Generally an application is made up of different layers:
- Interface: user communication with app
- Business: logic app
- Data: save data

Each layer knows its neighboring layer and can communicate with it but not how it works.

In this proyect will implement test in a movies app.

**Package model**
**Classes:**
Movie: id, name, minutes and genre.
Two contructors.

Genre: enum list: ACTION, COMEDY, DRAMA, HORROR, THRILLER.

**Data**
MovieRepository: Save movies in bbdd

**Package Service**
MovieService: logic business

We will start with business test.

**MovieServiceShould**
We'll start by asking what we want our service to do.

- Return movies by genre
- Return movies by lenght

For that we need MovieRepository, for testing will implement a mock of this with mockito

Use a SetUp like a movies repository. Tag **@Before**: runs before the tests to prepare the environment.

# To developer
## Challenge Search movies by name
In our movies app we want to be able to search for movies by name.

Implement the findByName function in MovieService, and add a test to test that it works correctly. Note that we want this function to find movies that contain part of the given name, so if we search for “Super” we want to get movies like “Super 8” or “Superman.”

Hint: you can use the contains function.

If necessary, add more movies to the test, so that there are movies that contain the same words.

Try to get the function to return the movies even if we search for “super” in lower case.

Hint: you can use the toLowerCase function.

## Extra challenge: Search movies by director
We also want to add the director of the movies and be able to search for them by director.

Add the director attribute to the Movie class. You will also have to add it in the Movie constructors, and update the tests to indicate this information. You can enter made-up director names if you don't want to search for real names (e.g. “director1”, “director2”, etc). In tests it does not matter whether the data is invented.

Once you have added the director attribute, implement the findByDirector function in MovieService, and add a test to test that it works correctly. You can use the same technique as findByName, and let the search be based on part of the director's name.
