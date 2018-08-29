---
layout: post
title: INU 매트릭스 멘토링_코텍2차
date: 2018-08-23
tags: 코텍
---

INU 매트릭스 멘토링 2회차 이다.


이번 멘토링에는 우리 학교 송도 캠퍼스 바로 앞에 있는 코텍 회사에 직접 방문하였다.

##코텍 첫 방문

코텍의 회사는 인천대입구역에서 공대에서 내리면서 항상 왔다갔다 봐았던 정문 건너편 건물이었다.

멘토링이 진행되었던 곳은 코텍 사내 회의실이었다.
<p>
![20180823_182055](https://user-images.githubusercontent.com/42561360/44667759-a2339900-aa56-11e8-911d-52399901f05b.jpg)


<p>

##멘토링 진행 순서
멘토링을 맡아 주신분 : 기술 연구소_천성열 상무님
<p>
- 사내 전시회 내 제품 설명
- 회의실에서 디스플레이의 동향 설명
- 터치 유리 표면 처리
- 코텍의 연구직 현황과 임베디드시스템공학과의 분야
<p>

##제품 소개
기술 연구소 천성열 상무님을 따라 회의실 옆에 있던 전시회 준비실에 갔다.

보안사항이라 머릿속에서만 저장해야 한다.

간략하게 말하자면 의료용, 대형, 게임용등 여러군대에서 사용되는 디스플레이 현황과 내장된 기술에 대해 설명을 들었다.

##디스플레이 동향 설명

- 들으면서 급하게 그린 그림이라 조금 이상할수 있다.


#####1. 저항막 방식
공간이 비어 있는 부분이 있음 -> 압력을 주었을때 전류가 발생하여 터치

![image](https://user-images.githubusercontent.com/42561360/44721939-6d7f1a80-ab06-11e8-954d-fd3005a0dc4b.png)




#####2. IR 방식(Infra Red )
한쪽에서는 적외선 LED를 통해 transmit 하고 다른 한쪽에서는 적외선 신호를 받는다

-> 터치가 일어나면 receive 쪽의 적외선 신호가 달라짐

-> 여러개의 센서로 터치된 좌표를 얻을수있다.

######단점 : 보내는 쪽과 받는 쪽의 센서들로 인해 배젤이 두꺼워진다.




![image](https://user-images.githubusercontent.com/42561360/44721978-8e477000-ab06-11e8-94c4-3863fb11b7a1.png)

#####3. pcap 방식 (커패시터 방식)
Projected Capacitor의 약자

또다른 표기법으로는 p_cap

여러가닥의 가느다란 선들로 이루어져있음

구리나 은나노로 이루어져있는 metal mesh 나 인듐,주석 등으로 이루어진 가느다란 실을 이용


######단점 : 가격이 비싸다

![image](https://user-images.githubusercontent.com/42561360/44722018-aae3a800-ab06-11e8-9d09-a1a04d0ca706.png)





#####[3-1] On-cell

pcap의 종류에서 TFT기판위에 터치 글라스가 있는 형태이다.

######단점 : 터치 글라스와 TFT와의 공간이 있어 패럴랙스가 생긴다.

초기의 터치 패널을 생각하면 된다.

![image](https://user-images.githubusercontent.com/42561360/44722033-bdf67800-ab06-11e8-8c1d-a28b4654f877.png)

#####[3-2] In-cell


On-cell의 단점인 왜곡을 보완하고자 생긴 형태이다.

TFT기판위에 바로 터치 글라스가 있다.

현재 스마트폰은 거의 모두 이런 방식을 사용한다고 한다.

###### 단점 : 일체형이어서 교체가 어렵다. 스마트폰 액정 교체시 비싼 이유이다.

![image](https://user-images.githubusercontent.com/42561360/44722044-c9e23a00-ab06-11e8-8750-24d52061d50e.png)


#####4.카메라 방식

터치한곳의 좌표를 알려면 최소 두개의 카메라가 필요하다.

터피 패널 끝이 reflector 로 이루어져 있어 IR을 보내고 반사되어 온 IR신호를 감지하여 좌표를 얻는다.

![image](https://user-images.githubusercontent.com/42561360/44722062-d5cdfc00-ab06-11e8-875d-ba9d4d7d425f.png)

#####5. In-glass 방식

전반사를 이용한 방식이다.

######단점 : 가격이 비싸다.<p>인식도가 낮다.

![image](https://user-images.githubusercontent.com/42561360/44722086-e8e0cc00-ab06-11e8-9004-44ba192c5537.png)

#####6. In-glass의 개선안

작은 reflector를 두어 IR신호를 주고 받는다.

삼성에서 최근에 상용 45인치로 출시하였다.

######단점: 여전히 비싸다는 문제점은 남아있다.




![image](https://user-images.githubusercontent.com/42561360/44723563-542c9d00-ab0b-11e8-8955-e7659c99c7bb.png)


##디스플레이 동향 설명

터치 디스플레이 분야에서는 유리 표면 처리가 매우 중요하다!

#####1. AG(anti-glare)
눈이 덜 부심 , 부드러운 필기감

#####2. AR(anti-reflective)

#####3. AG(anti-finger)



##코텍 연구직 현황과 임베디드시스템공학과의 분야

코텍의 기술연구 분야는 크게 4가지로 나뉜다고 한다.

#####1. 기구설계 분야

디스플레이의 전체 외양등 뼈대 같은 것을 설계하고 디자인하는 연구를 한다고 한다.

###### 학과 : 주로 기계과 , 기계 설계과 졸업자가 많다고 한다.

#####2. hardware 설계

회로를 직접 설계하고 최적의 배치를 찾는 분야이다.

###### 학과 : 전자공학과
###### 중요시 해야하는 전공 과목 : 회로이론,디지털논리설계 , 컴퓨터 아키텍쳐, 물리, 전자기학

#####3. firmware 설계

하드웨어에 대한 지식을 바탕으로 구동할 소프트웨어를 이어주는 드라이버,마법사와 같은 것을 개발하는 연구

딱 우리 학과에 맞는 분야이다.

실제로 우리 임베과 졸업생 재직자 4명정도 된다고 하셨다.

###### 학과 : 임베디드시스템공학과
###### 중요시 해야하는 과목 : 회로이론, 디지털논리설계 , 컴퓨터 아키텍쳐 , c c++ matlab 등 다양한 프로드래밍 언어, 데이터 구조 

##### 4.software 설계 

디스플레이의 다양한 기능을 프로그래밍하는 분야

###### 학과 : 임베디드시스템공학과 , 컴퓨터공학과
###### 중요시 해야하는 과목 : 다양한 언어 , 여러 기초 과목




![20180823_181345_162 2](https://user-images.githubusercontent.com/42561360/44723505-28a9b280-ab0b-11e8-86c4-397b4bbc4a0e.jpg)
