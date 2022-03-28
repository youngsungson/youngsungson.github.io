---
layout: post
title:  "저가형 윈도우태블릿 필수 최적 설정"
subtitle:   "Antimalware Service Executable 예외처리"
categories: stuffs
tags: stuff windows10 laptop
comments: true
header-img: img/stuffs/20180127-stuffs-lowcost-laptop.jpeg
---

## 개요
> 성능이 낮은 저가형 랩탑을 사용하면, 처음에는 쓸만한데.. 조금만 지나면 지나치게 느려진다. 해결책을 찾아보자 

저가형 윈도우태블릿을 사용하면 처음에는 사용할 만한데..

얼마 못가 갑자기 느려져서 인내력의 한계를 시험하다가 사용을 포기하는 단계로 들어가게 된다.

아무래도 아톰 CPU 태블릿 자체의 성능 한계도 있지만,

이유 모를 속도 저하가 의심스러워 찾아보니

Windows10 에 기본으로 들어간 Microsoft Security Essential (이하 MSE) 가 백그라운드로 돌면서 CPU를 적게는 10% 에서 많게는 50% 까지 차지하고 있는 현상이 있다.

원인은 이해하기 힘들지만, 바이러스 감시 서비스인데..

부팅한 뒤에 Antimalware Service Executable Process 가 셀프 감시(?)를 하는게 문제라는 리포트가 있어, 예외 처리를 하면 된다고 해서 그렇게 설정하니 CPU 점유율로 줄고.. 
윈도우 태블릿의 반응속도도  초기화한 것처럼시원하게 좋아졌다.

방법은 다음과 같다.

윈도우 – 설정 – 업데이트 및 복구 – Windows Defender – Windows Defender 보안 센터 열기 – 바이러스 및 위협방지 – 바이러스 및 위협방지 설정 – 제외 추가 및 제거 – 제외 사항 추가

이 메뉴를 통해서 3가지를 등록한다

  – 파일 : C:/Program Files/Windows Defender/MsMpEng.exe
  – 폴더 : C:/Program Files/Windows Defender/
  – 프로세스 : Antimalware Service Executable

이렇게 설정하고 재부팅을 하고 작업관리자를 보면 낮은 CPU 점유율을 볼 수 있다.

시험한 장비 : Teclast x89, Dell Venu 11 Pro 4300y

(제일 정확한 것은 Antimalware Service Executable 실행을 막는 것이다)

단, V3 를 사용하는 경우 위의 메뉴가 나타나지 않는다.

#Windows10 #저가형랩탑
