# SELECT NOBEL ANSWERS #
Completed in Sept. 30 2019 :octocat:
> Link: https://sqlzoo.net/wiki/SELECT_from_Nobel_Tutorial

**1.**
```mysql
SELECT yr, subject, winner FROM nobel
WHERE yr = 1950
```
**2.**
```mysql
SELECT winner FROM nobel
WHERE yr = 1962 AND subject = 'Literature'
```
**3.**
```mysql
SELECT yr, subject FROM nobel
WHERE winner = 'Albert Einstein'
```
**4.**
```mysql
SELECT winner FROM nobel
WHERE subject = 'Peace' and yr >= 2000
```
**5.**
```mysql
SELECT * FROM nobel
WHERE yr BETWEEN 1980 AND 1989
AND subject = 'Literature'
```
**6.**
```mysql
SELECT * FROM nobel
 WHERE winner IN ('Theodore Roosevelt',
'Jimmy Carter', 'Barack Obama', 'Woodrow Wilson') 
```
**7.**
```mysql
SELECT winner from nobel
WHERE winner LIKE 'John%'
```
**8.**
```mysql
SELECT yr, subject, winner FROM nobel
WHERE subject = 'Physics' AND yr = 1980
OR subject = 'Chemistry' AND yr = 1984
```
**9.**
```mysql
SELECT yr, subject, winner FROM nobel
WHERE yr = 1980 and subject NOT IN('Chemistry', 'Medicine')
```
**10.**
```mysql
SELECT yr, subject, winner FROM nobel
WHERE subject = 'Medicine' AND yr < 1910
OR  subject = 'Literature' AND yr >= 2004
```
### HARDER QUESTIONS ###
**11. Umlaut**
```mysql
SELECT * FROM nobel
WHERE winner = 'PETER GRÜNBERG'
```
**12. Apostrophe**
```mysql
SELECT * FROM nobel
WHERE winner = 'EUGENE O''NEILL'
```
**13.**
```mysql
SELECT winner, yr, subject FROM nobel
WHERE winner LIKE 'Sir%'
ORDER BY yr DESC, winner
```
