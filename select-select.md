# SELECT FROM SELECT ANSWER KEY #
Completed in September 30, 2019 :octocat:
> Link https://sqlzoo.net/wiki/SELECT_within_SELECT_Tutorial

**1.**
```mysql
SELECT name FROM world
WHERE population >
(SELECT population FROM world WHERE name='Russia')
```
**2.**
```mysql
SELECT name FROM world
WHERE continent = 'Europe' AND gdp/population >
(SELECT gdp/population FROM world WHERE name = 'United Kingdom')
```
**3.**
```mysql
SELECT name, continent FROM world
WHERE continent IN (SELECT continent FROM world
WHERE name IN ('Argentina','Australia'))
ORDER BY name
```
**4.**
```mysql
SELECT name, population FROM world
WHERE population > (SELECT population FROM world 
WHERE name = 'Canada') AND population < (SELECT population 
FROM world WHERE name = 'Poland')
```
**5.**
```mysql
SELECT name, CONCAT(ROUND(population/(SELECT population FROM world 
WHERE name = 'Germany')*100,0),'%') FROM world 
WHERE continent = 'Europe' 
```
**6.**
```mysql
SELECT name FROM world
WHERE gdp > ALL(SELECT gdp FROM world 
WHERE continent = 'Europe' AND gdp IS NOT NULL) 
```
**7.**
```mysql
SELECT continent, name, area FROM world x
WHERE area >= ALL
(SELECT area FROM world y 
WHERE y.continent=x.continent AND area>0)
```
**8.**
```mysql
SELECT continent, MIN(name) AS name
FROM world 
GROUP BY continent
ORDER by continent
```
**9.**
```mysql
SELECT name, continent, population FROM world x
WHERE 25000000 >= ALL(SELECT population FROM world y
WHERE y.continent = x.continent AND y.population IS NOT NULL)
```
**10.**
```mysql
SELECT name, continent FROM world x
WHERE population >= ALL(SELECT population * 3 FROM world y
WHERE y.continent = x.continent AND y.name != x.name)
```
