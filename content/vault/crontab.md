+++
draft = false
title = 'Crontab'
tags = ['linux']
+++

```sh
crontab -l
crontab -e
```


```
* * * * * COMMAND

minute(0-59) hour(0-23) day(1-31) month(1-12) weekday(0-7)
```

### Cheatsheet

- `* * * * *`: 매 분
- `5 * * * *`: 매 시 5분
- `10,40 * * * *`: 매 시 10분, 40분
- `0 12 * * 1`: 매 주 월요일 12:00
- `30 */6 * * *`: 6시간마다 30분
  - 00:30
  - 06:30
  - 12:30
  - 18:30
- `0 6 * * 1-5`: 월-금 06:00
