# Business_case_studies
Business case studies across e-commerce, SaaS, fintech, and product analytics.

## Business Request

The Content Strategy Team needs to understand what genres are popular in which countries. They want a breakdown of total watch time by country and genre to optimise regional content licensing.

```mysql
select u.country_code, c.genre, SUM(v.watch_minutes) as total_minutes, 
from viewing_sessions v
join users u on v.user_id = u.user_id
join content c on v.content_id = c.content_id
group by u.country_code, c.genre
order by total_watch_time desc
```

<img width="739" height="288" alt="image" src="https://github.com/user-attachments/assets/d631908e-d09a-439c-b384-0733feda9ccf" />
