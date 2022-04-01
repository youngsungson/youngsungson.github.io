---
layout: post
title:  "Offline RL 기법 논문들"
subtitle:   "박준영님이 소개해준 AWAC 논문, BAIR 팀 논문, 세르게이 르빈 교수 논문 입니다."
categories: dev
tags: dl deeplearning 딥러닝
comments: true
header-img: 
---

AI 프렌즈 세미나에서 소개된 Offline RL 기법의 논문들입니다. 박준영님이 소개해준 AWAC 논문, BAIR 팀 논문, 세르게이 르빈 교수 논문 입니다. 

저희 팀도 RL 에서 학습의 시간과 유효성에 대해서 고통을 받고 있어서, Offline RL 이라는 쌈빡(?)한 명칭과 개념에 대해서 반가운 마음으로 살펴봤습니다. 

아직 완전히 이해한 것이 아니라서.. 좀 불안하지만.. 

사람의 기보에서 바둑의 방법을 배웠던 알파고의 학습 개념이 아닌가 싶습니다. 

저희 연구팀도 End-to-End RL 학습이 잘 안되어서 전문가의 Behavior Cloning 기법을 활용해서 RL의 policy optimization을 해보고 있는데.. 

Offline RL 이 기존 Legacy System 의 operation log 를 활용해서 Model Contrstuction 을 하고 세부적인 최적화를 하는 것으로 보입니다. 

다만, 이런 방식의 한계는 레거시 시스템(전문가? 사람?)의 비효율성은 극복하기 어렵다는 것고.. action space 의 inregularity 문제에서 기인되는 학습의 불완전성이 여전히 문제입니다.. 

아마도 논문을 좀더 자세히 이해하면 해법이 포함되어 있을 것 같습니다. 

[AWAC: Accelerating Online Reinforcement Learning with Offline Datasets](https://openreview.net/forum?id=OJiM1R3jAtZ)

[Offline Reinforcement Learning: How Conservative Algorithms Can Enable New Applications](https://bair.berkeley.edu/blog/2020/12/07/offline/)

[Offline Reinforcement Learning: Tutorial, Review, and Perspectives on Open Problems](https://arxiv.org/pdf/2005.01643.pdf)

#AIFrenz #AI프렌즈 #OfflineRL
