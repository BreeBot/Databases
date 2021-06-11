With more practice, working with databases becomes second nature. To build our SQL skills, let's answer some questions relevant to our movies database.

## Getting Started

```no-highlight
et get database-drills
cd database-drills
dropdb movies
createdb movies
curl -o movie_database.sql.gz https://s3.amazonaws.com/launchacademy-downloads/movie_database.sql.gz
gunzip ./movie_database.sql.gz
psql movies
movies=# \i movie_database.sql
```

Write queries relevant to these questions in `questions.sql`

If your database ever gets corrupted and you'd like to start over, you can:

```no-highlight
dropdb movies
createdb movies
psql movies
movies=# \i movie_database.sql
```

## Retrieval

- What titles were released in 2003?
- What titles were released in 2004 and had a rating higher than 90?
- What actors have the last name of Wilson?
- What actors have the first name of Owen?
- What studios start with "Fox"?
- What studios involve Disney?
- What were the top 5 rated movies in 2005?
- What were the worst 10 movie titles and their ratings in 2000?

## Advanced Retrieval

- What movie titles were produced by Walt Disney Pictures in 2010?
- Who were the characters in "The Hunger Games"?
- Who acted in "The Hunger Games"?
- Who acted in a Star Wars movie? Be sure to include all movies.
- What were all of the character names for movies released in 2009?
- What are the character names in the "The Dark Knight Rises"?
- What actors and actresses have been hired by Buena Vista?

## Updating

- Troll 2 was the best movie ever. Let's update it to have a rating of 500.
- "Police Academy 4 - Citizens on Patrol" was underrated. Let's give it a 20.
- Matt Damon has updated his name to "The Artist Formerly Known as Matt Damon". Let's update the database to reflect this momentous change in the film industry.

## Deletion

- We want to forget Back to the Future Part III ever happened. Delete only that movie. Be sure to delete correlating `cast_member` entries first.
- Horror movies are too scary - delete every Horror movie. Don't forget about their correlating `cast_members` entries.
- Ben Affleck movies are also too scary - delete every movie he acted in. Wasn't that therapeutic?
- Fake news - we're revising history for 20th Century Fox. Delete any movie they produced that has a rating of less than 80.

## Schema

- We're creating a reviews table so that we can store individual movie reviews. The table should have a description, score from 0-100, author name, and it should relate to a movie. Create the DDL necessary to create this table.
- We're creating a crimes table for all crimes actors or actresses commit. It should include the year of offense, the title of the offense, and it should relate to the actor. Create the DDL necessary to create this table.
