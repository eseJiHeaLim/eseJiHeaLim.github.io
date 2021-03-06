---
layout: post
title: linux 커멘드 정리
date: 2019-07-30
tags: linux,raspberry
---

**//파일 관리 **  
ls : 현재 디렉토리의 목록을 보여준다  
ls -l : 디렉토리 안 파일들의 추가 정보를 보여준다. 권한/사이즈/시간/등등등   
ls -a : 디렉토리 내 dotfiles 를 보여준다   

cd : 디렉토리 이동   

pwd : 현재 있는 디렉토리 위치를 알려준다   

mkdir : 디렉토리를 만들어주는 명령어   

rmdir : 디렉토리가 비어있을때만 디렉토리를 지우는 명령어  

rm : 파일을 삭제하는 명령어  
rm -r : 디렉토리를 삭제하는 명령어  

cp : 파일을 복사해주는 명령어 , cp_복사할 파일_이동되는 곳  

mv : 파일 이동, mv file /home/pi  


**//파일 생성**  
touch : 빈 파일을 만들어 주는 명령어 , touch_파일명  
touch -c : 파일 날짜정보를 현재 시간으로 변경  
touch -t 201904241736 : 파일 날짜정보를 원하는 대로 변경  
touch -r : 파일의 날짜 정보를 똑같이 설정해주는 명령어  

**//파일 보기**  
cat : 파일 내용을 보여주는 명령어  

head : 파일 내용을 보여주는 명령어  
head -n : 파일내용 중 첫 줄부터 원하는 줄수 만큼 보여주는 명령어  

tail : 파일 내용을 보여주는 명령어  
tail -n : 파일 내용중 마지막 줄부터 원하는 줄수 만큼 보여주는 명령어  

**//파일 권한**  
chmod : 파일 권한을 바꿔주는 명령어 ,u 유저 g 그룹 ,o 제3자 , chmod u+x filename == filename의 유저에 접근권한을 준다 
sudo : superuser 모드  

**//파일 권한 정보** 
맨 앞 첫 글자 
- : 파일  
d : 디렉토리 

소유자-소유그룹-제3자 

r : 읽기 권한  
w : 쓰기 권한  
x : 접근 권한  
접근 권한이 있어야 rw가 가능하다  
 
**//디스크 관리 **  
df : 디스크 공간을 보여주는 명령어  
df -h : 사람이 읽을 수 있는 파일 사이즈로 디스크 공간을 출력해준다. M,GB 등  

**// 파일 압축 **  
unzip : 파일 압축을 풀어주는 명령어  

tar : 압축, 압축 푸는 명령어  
tar -cvf : .tar 파일로 파일들을 묶어줌  
tar -xvf : .tar 파일 압축 풀기  
tar -zcvf : .tar.gz 파일로 묶어서 압축  
tar -zxvf : .tar.gz 파일 압축 풀기  

**//파일 다운로드**  
wget : 인터넷으로 부터 파일 다운로드  
curl : 서버로부터 파일을 다운로드, 업로드  

man : 메뉴얼 보기  

**//검색 **  
grep : 원하는 키워드 검색  
find : 디렉토리 검색  
whereis : 원하는 파일, 디렉토리의 위치 검색  