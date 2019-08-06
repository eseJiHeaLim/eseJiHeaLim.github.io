---
layout: post
title: dotfile 이란?
date: 2019-04-24
tags: linux, raspberry pi
---

dotfile :
<p>
. 으로 시작하는 파일로 리눅스, 유닉스에서 숨김파일로 보이는 파일
<p>
~~~bash
pi@JH_raspberrypi:~/2017MidTerm $ ls 


num5.py  num6.py 
pi@JH_raspberrypi:~/2017MidTerm $ ls -a 


.  ..  num5.py  num6.py  .testdotfile.txt 
~~~
<p>
ls 로 파일목록을 확인이 불가하며 ls -a 명령을 사용하여 dotfiles를 확인 할수 있다.