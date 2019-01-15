---
layout: post
title: 문자추출 도전1_binarization
date: 2019-01-15
tags: 문자추출, computer vision
---

## binarization (이진화)

이미지의 모든 픽셀을 이진화, 흑과 백으로만 표현한것

256단계의 밝기로 나타내는 grayscale과는 다른것이었다.

threshold를 기준으로 낮으면 0 높으면 1또는 255로 설정한다

--> 물체의 특징 검출 및 처리해야할 데이터의 양을 줄일수있다.


## MATLAB으로 구현한 binarization
~~~matlab
clc;
clear;

%original image 가져오기
img= imread("name.png");

% image grayscale로 변경
img_g=rgb2gray(img);

% 모든 픽셀의 합을 구한다
allPixel=0;
temp= sum(img_g);

% threshold를 기준으로 이진변환
for i=1:2100
    allPixel= allPixel+temp(i);
end

 % 모든 합의 셀의 갯수로 나눠 threshold 값을 구한다
PixelCnt=2100*2100;
threshold=allPixel/(PixelCnt);

img_b=[];
% threshold를 기준으로 흑과 백으로 바꿔준다
for i=1:2100
    for j=1:2100
        if (img_g(i,j)<threshold)
            img_b(i,j)=0;
        else
            img_b(i,j)=1;
        end
    end
end

figure(1);
subplot(2,2,1)
imshow(img)
title('original image')
subplot(2,2,2)
imshow(img_g)
title('grayscale image')
subplot(2,2,3)
imshow(img_b)
title('binarization image')
subplot(2,2,4)
imshow(imbinarize(img_g))
title('matlab function binarization image')
~~~

![default](https://user-images.githubusercontent.com/42561360/51184147-c82edc80-1916-11e9-9fb7-76151f4f6f65.PNG)


## 문자 추출 도전
문자 추출을 알아보던중 보게된 전교수님 논문을 기준으로 모르는것을 알아간다.

첫 단계가 이진화였고 문자 추출관련 알고리즘에 대해 모르는것을 알아갈것이다
