### MORE JOIN ANSWER KEY ###
Completed in October 3, 2019 :octocat:
> Link: https://sqlzoo.net/wiki/More_JOIN_operations

**1.**
```
SELECT id, title
FROM movie
WHERE yr=1962
```
**2.**
```
SELECT yr AS year 
FROM movie
WHERE title = 'Citizen Kane'
```
**3.**
```
SELECT id, title, yr
FROM movie 
WHERE title LIKE '%Star Trek%'
ORDER BY yr
```
**4.**
```
SELECT id 
FROM actor
WHERE name = 'Glenn Close'
```
**5.**
```
SELECT id
FROM movie
WHERE title = 'Casablanca'
```
**6.**
```
SELECT name
FROM casting 
INNER JOIN actor on actorid = actor.id
INNER JOIN movie ON movieid =movie.id
WHERE movieid = 11768
```
**7.**
```
SELECT name
FROM casting 
INNER JOIN actor on actorid = actor.id
INNER JOIN movie ON movieid =movie.id
WHERE title = 'Alien'
```
**8.**
```
SELECT title 
FROM movie 
INNER JOIN casting ON movie.id = movieid
INNER JOIN actor ON actor.id = actorid
WHERE name = 'Harrison Ford' 
```
**9.**
```
SELECT title 
FROM movie 
INNER JOIN casting ON movie.id = movieid
INNER JOIN actor ON actor.id = actorid
WHERE name = 'Harrison Ford'  AND ord != 1
```
**10.**
```
SELECT title, name
FROM movie 
INNER JOIN casting ON movie.id = movieid
INNER JOIN actor ON actor.id = actorid
WHERE yr = 1962 AND ord = 1
```
