# SELECT COUNT ANSWER KEY #
Completed in September 30, 2019 :octocat:
> Link: https://sqlzoo.net/wiki/SUM_and_COUNT

**1. Show the total population of the world**
```mysql
SELECT SUM(population)
FROM world
```
**2. List all the continents - just once each.**
```mysql
SELECT continent FROM world
GROUP BY continent
```
**3. Give the total GDP of Africa**
```mysql
SELECT SUM(gdp) FROM world
WHERE continent = 'Africa'
```
**4. Count the big countries**
```mysql
SELECT COUNT(name) FROM world
WHERE area >= 1000000
```
**5. Total population of Estonia, Latvia, Lithuania**
```mysql
SELECT SUM(population) FROM world
WHERE name IN('Estonia', 'Latvia','Lithuania')
```
**6. Show the continent and number of countries.**
```mysql
SELECT continent, COUNT(name) FROM world
GROUP BY continent
```
**7. Show the continent and number of countries with populations of at least 10 M**
```mysql
SELECT continent, COUNT(name) FROM world
WHERE population >= 10000000
GROUP BY continent
```
**8. Continents that have a total population of at least 100 M**
```mysql
SELECT continent FROM world
GROUP BY continent
HAVING SUM(population) > 100000000
```
