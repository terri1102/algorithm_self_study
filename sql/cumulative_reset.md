![image](https://user-images.githubusercontent.com/73813367/127149730-0a4034ae-1039-4099-80eb-16df13547b4e.png)

[sqlite db]

1. text를 Datetime으로 변환(원래 문제에선 Datetime이었지만...sqlite db 만드는 과정에서 실수함)

2. Datetime을 Date로 변환

```sql
SELECT DATE_FORMAT(created_at, '%y-%m-%d') AS Date
FROM test
```
3. window function으로 cumulative count reset
