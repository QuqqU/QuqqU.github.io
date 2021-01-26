---
title: QuqqU - SQL REGEXP
description: SQL Regex
header: HackerRank Weather Observation Station 7
duration: 1 minutes read
---


### [문제 링크](https://www.hackerrank.com/challenges/weather-observation-station-7/problem?h_r=next-challenge&h_v=zen)

## 그저... 노가다 패턴매칭
```sql
select 
    distinct city
from
    station
where
    city like '%a' or
    city like '%e' or
    city like '%i' or
    city like '%o' or
    city like '%u';
```

## 정규표현식 사용
```sql
select 
    distinct city
from
    station
where
    city rlike '[aeiou]$';
```

RLILE 대신에 REGEXP를 사용할 수 있다.

```sql
select 
    distinct city
from
    station
where
    city regexp '[aeiou]$';
```
#### 결론 : LIKE 버리고 REGEXP 사용하자.
