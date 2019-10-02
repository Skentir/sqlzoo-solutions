# JOIN ANSWER-KEY #
Completed in October 2, 2019 :octocat:
> Link: https://www.w3schools.com/sql/exercise.asp?filename=exercise_join1

**1.**
```
SELECT matchid, player 
FROM goal 
WHERE teamid = 'GER'
```
**2.**
```
SELECT id,stadium,team1,team2
FROM game WHERE id = '1012'
```
**3.**
```
SELECT player, teamid, stadium, mdate
FROM game JOIN goal ON (id=matchid AND teamid = 'GER')
```
**4.**
```
SELECT team1, team2, player FROM game 
JOIN goal ON (id = matchid AND player LIKE 'Mario%')
```
**5.**
```
SELECT player, teamid, coach, gtime
FROM goal JOIN eteam ON (teamid = id)
WHERE gtime <=10
```
**6.**
```
SELECT mdate, teamname FROM game JOIN eteam 
ON (team1 = eteam.id AND coach = 'Fernando Santos') 
```
**7.**
```
SELECT player FROM goal 
JOIN  game ON matchid = id
WHERE stadium = 'National Stadium, Warsaw'
```
### HARDER QUESTIONS ### 
**8.**
```
SELECT DISTINCT(player)
FROM game JOIN goal ON matchid = id 
WHERE (team1='GER' OR team2 ='GER')
AND teamid != 'GER'
```
**9.**
```
SELECT teamname, COUNT(player)
FROM eteam JOIN goal ON id=teamid
GROUP BY teamname
```
**10.**
```
SELECT stadium, COUNT(matchid) FROM game 
JOIN goal ON (id = matchid)
GROUP BY stadium
```
**11.**
```
SELECT matchid, mdate, COUNT(player)
FROM game JOIN goal ON matchid = id 
WHERE (team1 = 'POL' OR team2 = 'POL')
GROUP BY matchid, mdate
```
