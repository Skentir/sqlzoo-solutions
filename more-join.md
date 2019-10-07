### MORE JOIN ANSWER KEY ###
Completed in October 3, 2019 :octocat:
> Link: https://sqlzoo.net/wiki/More_JOIN_operations

**1.**
```mysql
SELECT id, title
FROM movie
WHERE yr=1962
```
**2.**
```mysql
SELECT yr AS year 
FROM movie
WHERE title = 'Citizen Kane'
```
**3.**
```mysql
SELECT id, title, yr
FROM movie 
WHERE title LIKE '%Star Trek%'
ORDER BY yr
```
**4.**
```mysql
SELECT id 
FROM actor
WHERE name = 'Glenn Close'
```
**5.**
```mysql
SELECT id
FROM movie
WHERE title = 'Casablanca'
```
**6.**
```mysql
SELECT name
FROM casting 
INNER JOIN actor on actorid = actor.id
INNER JOIN movie ON movieid =movie.id
WHERE movieid = 11768
```
**7.**
```mysql
SELECT name
FROM casting 
INNER JOIN actor on actorid = actor.id
INNER JOIN movie ON movieid =movie.id
WHERE title = 'Alien'
```
**8.**
```mysql
SELECT title 
FROM movie 
INNER JOIN casting ON movie.id = movieid
INNER JOIN actor ON actor.id = actorid
WHERE name = 'Harrison Ford' 
```
**9.**
```mysql
SELECT title 
FROM movie 
INNER JOIN casting ON movie.id = movieid
INNER JOIN actor ON actor.id = actorid
WHERE name = 'Harrison Ford'  AND ord != 1
```
**10.**
```mysql
SELECT title, name
FROM movie 
INNER JOIN casting ON movie.id = movieid
INNER JOIN actor ON actor.id = actorid
WHERE yr = 1962 AND ord = 1
```
