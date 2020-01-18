# Pursuit-Core-Web-SQL-Lab

Complete the tutorial at the link [here](https://sqlbolt.com/lesson/select_queries_introduction)

Fork and clone this repo, then for each of the 18 sections, copy and paste your solution in your fork.  Submit by making a PR against this repo.

EX 1
1.  SELECT title FROM movies;
2.  SELECT director FROM movies;
3.  SELECT title, director 
    FROM  movies;
4.  SELECT title, year FROM movies;
5.  SELECT * FROM movies;

EX 2
1.  SELECT * FROM movies
    WHERE id = 6
2.  SELECT * FROM movies
    WHERE Year Between 2000 AND 2010
3.  SELECT * FROM movies
    WHERE Year Not Between 2000 AND 2010
4.  SELECT * FROM movies
    WHERE id Between 1 AND 5

EX 3
1.  SELECT * FROM movies
    WHERE Title Like "%Toy%Story%";
2.  SELECT * FROM movies
    WHERE Director = "John Lasseter"
3.  SELECT * FROM movies
    WHERE Director <> "John Lasseter"
4.  SELECT * FROM movies
    WHERE Title Like "WALL-%"

EX 4
1.  SELECT DISTINCT Director
    FROM Movies
    ORDER BY Director ASC
2.  SELECT *
    FROM Movies
    ORDER BY Year DESC
    LIMIT 4
3.  SELECT *
    FROM Movies
    ORDER BY Title asc
    LIMIT 5
4.  SELECT *
    FROM Movies
    ORDER BY Title asc
    LIMIT 5
    OFFSET 5

RV 1 
1.  SELECT * FROM                   north_american_cities
    WHERE Country = "Canada"
2.  SELECT * FROM   north_american_cities
    WHERE Country = "United States"
    ORDER BY Latitude DESC
3.  SELECT * FROM   north_american_cities
    WHERE  Longitude <	-87.629798
    ORDER BY Longitude ASC
4.  SELECT * FROM north_american_cities
    WHERE  Country = "Mexico"
    ORDER BY Population desc
    LIMiT 2
5.  SELECT * FROM north_american_cities
    WHERE  Country = "United States"
    ORDER BY Population desc
    LIMiT 2
    OFFSET 2