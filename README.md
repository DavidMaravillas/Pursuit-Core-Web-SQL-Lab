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

EX 6
1.  SELECT Title, Domestic_sales,   International_sales
    FROM movies
    INNER JOIN Boxoffice
        ON Movies.Id = Boxoffice.Movie_id
2. SELECT Title, Domestic_sales, International_sales
    FROM movies
    INNER JOIN Boxoffice
        ON Movies.Id = Boxoffice.Movie_id
    WHERE International_sales >     Domestic_sales
3.  SELECT *
    FROM movies
    INNER JOIN Boxoffice
        ON Movies.Id = Boxoffice.Movie_id
    ORDER BY Rating DESC

EX 7
1.  SELECT DISTINCT Building 
    FROM Employees
    LEFT JOIN Buildings
    ON Building_name = Building
2.  SELECT DISTINCT Capacity,   Building_name
    FROM Buildings
    LEFT JOIN Employees
    ON Buildings.Building_name =        Employees.Building
3. SELECT DISTINCT Building_name,       Role
    FROM Buildings
    LEFT JOIN Employees
        ON Buildings.Building_name = Employees.Building

EX 8
1.  SELECT DISTINCT Name, Role 
    FROM employees
    WHERE Building IS NUll
2.  SELECT DISTINCT Building_name 
    FROM Buildings
    LEFT JOIN Employees 
        ON Building_name = Building
    WHERE Building IS NUll

EX. 9
1. SELECT Title, (Domestic_sales+International_sales)/1000000 
    AS Sales_Millions
FROM movies
INNER JOIN Boxoffice
    on Movies.Id = Boxoffice.Movie_id
2. SELECT Title, Rating*10
    AS Ratings_Percent
FROM movies
INNER JOIN Boxoffice
    on Movies.Id = Boxoffice.Movie_id
3. SELECT *
FROM movies
INNER JOIN Boxoffice
    on Movies.Id = Boxoffice.Movie_id
WHERE Year%2 = 0

EX 10
1. SELECT MAX(Years_employed) FROM employees
2.  SELECT Role, AVG(Years_employed)
    FROM employees
    GROUP BY role
3. SELECT BUIlding, SUM(Years_employed) FROM employees
GROUp BY BUIlding


EX 11
1. SELECT Sum(role="Artist") AS         Num_of_Artist
    FROM employees; 

2.  SELECT Role, count(role)FROM            employees
    GROUP by Role

3.  SELECT role, SUM(Years_employed)
    FROM employees
    WHERE ROle = "Engineer"

EX. 12
1. SELECT Director, count(Director) FROM movies
GROUP By Director
2. SELECT director, sum(Domestic_sales+International_sales)FROM movies
INNER JOIn Boxoffice
    on Boxoffice.Movie_id = Movies.Id
GROUP BY director

EX 13
1. INSERT INTO Movies
Values (4, "TOY STORY 4", "John Lasseter", 2019, 90)
2. INSERT INTO Boxoffice
values (4,8.7,340000000,270000000)

EX 14
1. 
UPDATE Movies
SET Director = "John Lasseter" 
WHERE Title = "A Bug's Life" ;
2.
UPDATE Movies
SET Year = 1999
WHERE Title = "Toy Story 2" ;
3.
UPDATE Movies
SET title = "Toy Story 2", Director = "Lee Unkrich"
WHERE Id = 11

EX 15
1. 
DELETE FROM Movies
WHERE Year <= 2005;
2.
DELETE FROM Movies
WHERE Director = "Andrew Stanton";

EX 16
1.
CREATE TABLE Database (
    Name TEXT,
    Version FLOAT,
    Download_count INTEGER
);

EX 17
1.
ALTER TABLE Movies
ADD Aspect_ratio FLOAT;
2.
ALTER TABLE Movies
ADD Language TEXT
    DEFAULT "English";
EX 18
1. DROP TABLE IF EXISTS Movies

2. DROP TABLE IF EXISTS Boxoffice;