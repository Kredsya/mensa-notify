# mensa-notify

멘사 테스트 공지가 올라왔는지 확인하고, 새로운 테스트가 생겼을 경우 디스코드 웹훅으로 알려주는 프로그램

## How to use

### start setting

```bash
$ git clone https://github.com/Kredsya/mensa-notify.git
$ crontab -e
```
and add a line `0 9 * * * python3 /path/to/mensa-notify.py` (run python at 9 a.m. everyday). If you want to custum the time, refer to the result of `crontab -h`.

### stop

```bash
$ crontab -r
```

or delete a line when you started.

## 개발 동기

오랜만에 [멘사](https://www.mensakorea.org/)에서 테스트를 재개하였다.

그전엔 자주 들어가서 새로운 테스트가 올라왔는지 계속 확인했었는데 bob에 신경이 쏠리면서 확인을 못하자마자 테스트가 올라와서 놓치고 말았다.

이에 분노하여 하루에 한 번 확인하고자 하였으나, 내가 하기에는 귀찮으니 라파에게 일을 시킬 것이다.

## 구현 아이디어

리눅스의 crontab으로 하루에 한 번 `python3 mensa-notify.py`를 실행한다.

만약 내가 원하는 [테스트 공지](https://www.mensakorea.org/bbs/board.php?bo_table=test)(지금 원하는건 25년 5월)가 올라오면 디스코드 웹훅으로 해당 사실을 보낸다.

## License

[Beerware License](LICENSE)
