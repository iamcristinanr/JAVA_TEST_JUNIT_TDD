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
