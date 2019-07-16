---
layout: post
title: 커맨드라인에서 팀뷰어 실행 및 아이디를 알아내기
date: 2019-07-16
tags: 리눅스, 팀뷰어, 커맨드
---

putty로 ssh를 사용하다가도 이미지를 확인하기 위해서 등의 이유로 팀뷰어나 vnc를 사용해야하는 경우가 있다. 

개인적으로 속도가 느린 vnc 보다는 teamviwer를 선호하여 teamviwer를 커맨드라인에서 실행시키고 아이디를 알아내어 연결을 해보고자 한다.

teamviwer를 설치한후 서비스를 시작 시키는 커맨드는 아래와 같다. 

```
sudo systemctl start teamviewerd.service
```


위와 같이 서비스를 시작한 후 에는 아래 커맨드를 입력하여 teamviwer에 대한 	정보를 획득 할 수 있다.

```
/usr/bin/teamviewer --info
```
