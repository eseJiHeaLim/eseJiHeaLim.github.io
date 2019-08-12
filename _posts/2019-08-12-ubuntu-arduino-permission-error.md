---
layout: post
title: ubuntu arduino 포트 권한 에러 해결법
date: 2019-08-12
tags: linux, ubuntu, arduino
---

우분투 14.04에 아두이노를 설치 한 후 프로그램을 업로드 하려 했으나 다음과 같은 에러가 발생한다.   
avrdude: ser_open(): can't open device "/dev/ttyACM0": Permission denied  
보드에 업로딩중에 문제 발생. 다음을  참고하세요. http://www.arduino.cc/en/Guide/Troubleshooting#upload  

포트 권한 문제를 해결하기 위해서 입력해야 하는 커맨드는 다음과 같다.   

~~~bash  

sudo usermod -a -G dialout 호스트네임(jihealim)
sudo chmod a+rw /dev/ttyACM1

~~~  

그 후에 다시 업로드 하면 아주 정상적으로 업로딩이 된다.   
하지만 또 다른 문제점이 있다.  
케이블을 뽑고 다시 연결 할 때 마다 달라지는 포트 번호로 매번 다시 권한을 설정 해 줘야한다는 것이다.  


위 문제를 해결하기 위해 조금 더 알아봐야겠다.  
혹시 이 글을 본 사람 중 해결법을 아는 사람이 있다면 연락 부탁 드립니다.  

