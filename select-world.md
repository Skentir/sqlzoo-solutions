# SELECT FROM WORLD ANSWERS 
 Completed in Sep. 30, 2019 :octocat:
> Link: https://sqlzoo.net/wiki/SELECT_from_WORLD_Tutorial

**1.**
```mysql
SELECT name, continent, population FROM world
```
**2.**
```mysql
SELECT name FROM world
WHERE population >= 200000000
```
**3.**
```mysql
SELECT name, gdp/population FROM world
WHERE population > 200000000
```
**4.**
```mysql
SELECT name, population/1000000
FROM world
WHERE continent = 'South America'
```
**5.**
```mysql
SELECT name, population FROM world
WHERE name IN ('France', 'Germany', 'Italy')
```
**6.**
```mysql
SELECT name FROM world
WHERE name LIKE '%United%'
```
**7.**
```mysql
SELECT name, population, area FROM world
WHERE population > 250000000 OR area > 3000000
```
**8.**
```mysql
SELECT name, population, area FROM world
WHERE population > 250000000 XOR area > 3000000
```
**9.**
```mysql
SELECT name, ROUND(population/1000000,2), ROUND(gdp/1000000000,2) FROM world
WHERE continent = 'South America'
```
**10.**
```mysql
SELECT name, ROUND(gdp/population,-3)
FROM world
WHERE gdp >= 1000000000000
```
**11.**
```mysql
SELECT name, capital FROM world
WHERE LENGTH(name) = LENGTH(capital) 
```
**12.**
```mysql
SELECT name, capital
FROM world
WHERE LEFT(name,1) = LEFT(capital,1) AND name <> capital
```
**13.**
```mysql
SELECT name FROM world
WHERE name LIKE '%a%'
AND name LIKE '%e%'
AND name LIKE '%i%'
AND name LIKE '%o%'
AND name LIKE '%u%'
AND name NOT LIKE '% %'
```
