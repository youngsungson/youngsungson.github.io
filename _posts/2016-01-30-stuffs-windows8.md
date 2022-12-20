---
layout: post
title:  "Windows8.1 권한 문제"
subtitle:   "Please login with administrator privilege and try again"
categories: stuffs
tags: stuff windows8 
comments: true
header-img: 
---

## 개요
> Windows8.1 권한 문제를 해결하자 

Windows8.1 에서 프로그램 실행시 다음 문제점
Please login with administrator privileges and try again


sc config secdrv start= demand
sc start secdrv


위 명령을 실행하면 권한 문제 없이 해결됨.


따라서..


batch 파일을 만들어서 사용하면 편리함.
물런 관리자 권한으로 실행해야 함.


start-secdrv.bat:
start cmd.exe /k "sc config secdrv start=demand"
start cmd.exe /k "sc start secdrv"




stop-secdrv.bat
start cmd.exe /k "sc stop secdrv"
start cmd.exe /k "sc config secdrv start=disabled"

#Windows8 
