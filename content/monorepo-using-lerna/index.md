---
emoji: ๐ชจ
title: '[React] Lerna๋ก Mono-Repo ๊ตฌ์ถํ๊ธฐ'
date: '2022-03-29 23:00:00'
author: ์์ ๋ฆผ
tags: react
categories: react
---

## Mono-Repo vs Multi-Repo

### Multi-Repo

`Multi-Repo` ๋ ์ฌ๋ฌ repository์ `package`๋ฅผ ๋ถ์ฐํด ๋๋ ๊ฒ์ ์๋ฏธํ๋ค. -> ์ผ๋ฐ์ ์ธ ๊ตฌ์ฑ

- ํ๋ ๋๋ ๋๊ฐ ์ด์์ pacakge ๊ด๋ฆฌ๋ฅผ ํ๋ ๋๋ ๋๊ฐ ์ด์์ repository๋ก ๊ตฌ์ฑํ์ฌ ๊ด๋ฆฌํ๋ค. 
- Package ๋ณ๋ก repository๋ฅผ ๋ถ๋ฆฌํ๋ค.

๐ ์ฅ์ 
- Repository ๋ณ owner๋ฅผ ์ง์ 
- ๋น ๋ฅธ CI Build
- ํจํค์ง์ ๋ชํํ ๋ถ๋ฆฌ๋ก ์ธํ ์ ์ฐ์ฑ ํฅ์

๐ ๋จ์ 
- ์ค๋ณต๋ ์ค์  ๋ฐ ๋ฐ๋ณต๋ ์ค์น
- ์ด์์ ๋ถ์ฐ
- Dependency hell
- ์ค๋ณต ์ฝ๋์ ๊ฐ๋ฅ์ฑ
