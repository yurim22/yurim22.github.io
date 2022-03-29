---
emoji: 🪨
title: '[React] Lerna로 Mono-Repo 구축하기'
date: '2022-03-29 23:00:00'
author: 서유림
tags: react
categories: react
---

## Mono-Repo vs Multi-Repo

### Multi-Repo

`Multi-Repo` 는 여러 repository에 `package`를 분산해 두는 것을 의미한다. -> 일반적인 구성

- 하나 또는 두개 이상의 pacakge 관리를 하나 또는 두개 이상의 repository로 구성하여 관리한다. 
- Package 별로 repository를 분리한다.

😇 장점
- Repository 별 owner를 지정
- 빠른 CI Build
- 패키지의 명확한 분리로 인한 유연성 향상

😈 단점
- 중복된 설정 및 반복된 설치
- 이슈의 분산
- Dependency hell
- 중복 코드의 가능성
