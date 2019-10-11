# MORE JOIN ANSWER KEY #
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
### HARDER QUESTIONS ###
**11.**
```mysql
SELECT yr,COUNT(title) FROM
  movie JOIN casting ON movie.id=movieid
        JOIN actor   ON actorid=actor.id
WHERE name='Doris Day'
GROUP BY yr
HAVING COUNT(title) > 1
```
**12.**
```mysql
SELECT movieid FROM casting
WHERE actorid IN (
  SELECT id FROM actor
  WHERE name='Julie Andrews')
```
**13.**
```mysql
SELECT a.name
FROM actor a
JOIN casting c ON a.id = c.actorid
WHERE c.ord = 1
GROUP BY a.name
HAVING COUNT(c.ord) >= 30
ORDER BY a.name
```
**14.**
```mysql
SELECT m.title, COUNT(c.actorid) as 'Num_of_Actors'
FROM movie m
JOIN casting c ON m.id = c.movieid
WHERE m.yr = 1978
GROUP BY m.title
ORDER BY COUNT(c.actorid) DESC, title
```
**15.**
```mysql
SELECT DISTINCT name FROM casting
JOIN actor ON actorid = actor.id
WHERE name != 'Art Garfunkel'
AND movieid IN (
		SELECT movieid
		FROM movie
		JOIN casting ON movieid = movie.id
		JOIN actor ON actorid = actor.id
		WHERE actor.name = 'Art Garfunkel'
)
```
