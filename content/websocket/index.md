---
emoji: ๐
title: '์น ๋ธ๋ผ์ฐ์ ์์์ ์๋ฐฉํฅ ํต์ '
date: '2022-03-22 23:00:00'
author: ์์ ๋ฆผ
tags: websocket
categories: networks 
---

## ์น ๋ธ๋ผ์ฐ์ ์์์ ์๋ฐฉํฅ ํต์ 

### โ ๏ธย ๊ธฐ์กด http ํ๋กํ ์ฝ์ ํ๊ณ

๊ธฐ์กด ์นํ์ด์ง์์ ์ฌ์ฉํ๋ http ํ๋กํ ์ฝ์ ์์ฒญ/์๋ต ํจ๋ฌ๋ค์์ด๊ธฐ์ ํด๋ผ์ด์ธํธ์์ ์์ฒญ์ ๋ณด๋ด์ผ๋ง ๊ทธ์ ๋ํ ์๋ต์ ๋ฐ์๋ค. http ํ๋กํ ์ฝ๋ก ํต์ ํ๋ ๊ฒฝ์ฐ, ํน์ฑ์ stateless์ด๊ธฐ ๋๋ฌธ์ ์ฐ๊ฒฐ์ด ์ ์ง๋์ง ์์ **์๋ฒ์์ ๋จผ์  ์์ฒญ์ ๋ณด๋ด๋ ๊ฒ์ด ๋ถ๊ฐ๋ฅ**ํ๋ค. 

### ๐งคย http ์ ๋์ฒด โ `Polling` , `Long Polling` , `Streaming`

- **Polling**
    
    : ํด๋ผ์ด์ธํธ์์ ์ผ์  ์ฃผ๊ธฐ๋ง๋ค ์์ฒญ์ ๋ณด๋ด๊ณ  ์๋ฒ๋ ํ์ฌ ์ํ๋ฅผ ๋ฐ๋ก ์๋ตํ๋ ๋ฐฉ์
    
    ๐ถย ์ด ๋ฐฉ์์ ๋ถํ์ํ ํธ๋ํฝ์ด ๋ฐ์ํ๊ธฐ ๋๋ฌธ์ ์ค์๊ฐ ๋ฐ์ดํฐ๊ฐ ์ค์ํ ์๋น์ค์๋ ์ข์ง ์๋ค.
    
- **Long Polling (event ์ค์ฌ)**
    
    : ํด๋ผ์ด์ธํธ์์ ์์ฒญ์ ๋ณด๋ด๊ณ  ์๋ฒ์์๋ ์ด๋ฒคํธ๊ฐ ๋ฐ์ํ์ ๋ ์๋ต์ ๋ด๋ ค์ค๋ค. ๊ทธ๋ฆฌ๊ณ  ํด๋ผ์ด์ธํธ๊ฐ ์๋ต์ ๋ฐ์์ ๋ ๋ค์ ๋ค์ ์๋ต์ ๊ธฐ๋ค๋ฆฌ๋ ์์ฒญ์ ๋ณด๋ธ๋ค.  
    
    ๐ถย ์ด ๋ฐฉ์์ ์ค์๊ฐ ๋ฐ์์ด ๊ฐ๋ฅํ๊ณ  polling์ ๋นํด์ ๋ถํ์ํ ํธ๋ํฝ์ ์ ๋ฐํ์ง ์์ง๋ง ์คํ๋ ค ์ด๋ฒคํธ๊ฐ ์ฆ๋ค๋ฉด ์๊ฐ์ ์ผ๋ก ๊ณผ๋ถํ๊ฐ ๊ฑธ๋ฆฐ๋ค.
    
- **Streaming**
    
    : ์ด๋ฒคํธ๊ฐ ๋ฐ์ํ์ ๋ ์๋ต์ ๋ด๋ ค์ฃผ๋๋ฐ ์๋ต์ ์๋ฃ์ํค์ง ์๊ณ  ๊ณ์ ์ฐ๊ฒฐ์ ์ ์งํ๋ ๋ฐฉ์
    
    ๐ถย  ์ด ๋ฐฉ์์ ์ฐ๊ฒฐ์๊ฐ์ด ๊ธธ์ด์ง์๋ก ์ฐ๊ฒฐ์ ์ ํจ์ฑ ๊ด๋ฆฌ์ ๋ถ๋ด์ด ๋ฐ์ํ๋ค. ๋์  ์ฐ๊ฒฐ์ด ์ ์ง๋์ด์๊ธฐ ๋๋ฌธ์ ์๋ต๋ง๋ค ๋ค์ ์์ฒญ์ ๋ณด๋ผ ํ์๋ ์๋ค.
    

### ๐ค๐ปย Websocket์ ๋ฑ์ฅ

HTML5์์ websocket์ ๊ฐ๋์ด ๋ฑ์ฅํ๋ฉด์ ์๋ฒ-ํด๋ผ์ด์ธํธ๊ฐ์ ์๋ฐฉํฅ ํต์ ์ ๊ตฌํํ  ์ ์๊ฒ ๋์๋ค.

### ๐ค๐ปย Websocket์ด๋?

์น ์๋ฒ์ ์น ๋ธ๋ผ์ฐ์ ๊ฐ ์ค์๊ฐ ์๋ฐฉํฅ ํต์ ํ๊ฒฝ์ ์ ๊ณตํด์ฃผ๋ ์ค์๊ฐ ํต์  ๊ธฐ์ ์ด๋ค. ์๋ฒ์ ๋ธ๋ผ์ฐ์  ๊ฐ์ ์ฐ๊ฒฐ์ ์ ์งํ ์ํ๋ก ๋ฐ์ดํฐ ๊ตํ์ด ์ด๋ฃจ์ด์ง๋ค. 

- ๋ฐ์ดํฐ ์ ๋ฌ ๋จ์ : ํจํท(packet)
- ์ ์ก์ ์ปค๋ฅ์ ์ค๋จ๊ณผ ์ถ๊ฐ http ์์ฒญ ์์ด ์๋ฐฉํฅ์ผ๋ก ์ด๋ค์ง๋ค.

์น์์ผ์ ์จ๋ผ์ธ ๊ฒ์์ด๋ ์ฃผ์ ํธ๋ ์ด๋ฉ ์์คํ ๊ฐ์ด ๋ฐ์ดํฐ ๊ตํ์ด ์ง์์ ์ผ๋ก ์ด๋ค์ ธ์ผ ํ๋ ์๋น์ค์ ์์ฃผ ์ ํฉํ๋ค.

![Untitled](./polling_websocket.png)

### ๐ค๐ปย Websocket ์์

์น์์ผ ์ปค๋ฅ์์ ๋ง๋ค๋ ค๋ฉด `new Websocket` ์ ํธ์ถํ๋ฉด ๋๋๋ฐ, ์ด๋ `ws` ๋ผ๋ ํน์ ํ๋กํ ์ฝ์ ์ฌ์ฉํ๋ค.

```jsx
let socket = new WebSocket("ws://yurim22.github.io");
// ("ws://url ์ฃผ์")
```

์์ผ์ด ์ ์์ ์ผ๋ก ๋ง๋ค์ด์ง๋ฉด ์๋ ๋ค ๊ฐ์ ์ด๋ฒคํธ๋ฅผ ์ฌ์ฉํ  ์ ์๋ค.

- `open` - ์ปค๋ฅ์์ด ์ ๋๋ก ๋ง๋ค์ด์ก์ ๋ ๋ฐ์ํจ
- `message` - ๋ฐ์ดํฐ๋ฅผ **์์ **ํ์์ ๋ ๋ฐ์ํจ
- `error` - ์๋ฌ๊ฐ ์๊ฒผ์ ๋ ๋ฐ์ํจ
- `close` - ์ปค๋ฅ์์ด ์ข๋ฃ๋์์ ๋ ๋ฐ์ํจ

์ปค๋ฅ์์ด ๋ง๋ค์ด์ง ์ํ์์ ๋ฌด์ธ๊ฐ๋ฅผ ๋ณด๋ด๊ณ  ์ถ์ผ๋ฉด `socket.send(data)` ๋ฅผ ์ฌ์ฉํ๋ฉด ๋ฉ๋๋ค.

```jsx
let socket = new WebSocket("wss://yurim22.github.io/websocket/demo/hello");

socket.onopen = function(e) {
	alert("[open] ์ปค๋ฅ์์ด ๋ง๋ค์ด์ก์ต๋๋ค.");
	alert("๋ฐ์ดํฐ๋ฅผ ์๋ฒ์ ์ ์กํด๋ด์๋ค.");
	socket.send("My name is yurim");  //๋ฐ์ดํฐ ์ ์ก
}

socket.onclose = function(event) {
	if(event.wasClean) {
		alert(`[close] ์ปค๋ฅ์์ด ์ ์์ ์ผ๋ก ์ข๋ฃ๋์์ต๋๋ค(code=${event.code} reason=${event.reason})`;
	} else {
		// ์์: ํ๋ก์ธ์ค๊ฐ ์ฃฝ๊ฑฐ๋ ๋คํธ์ํฌ์ ์ฅ์ ๊ฐ ์๋ ๊ฒฝ์ฐ
		// event.code === 1006
		alert('[close] ์ปค๋ฅ์์ด ์ฃฝ์์ต๋๋ค.');
	}
};

socket.onerror = function(error) {
	alert(`[error] ${error.message}`);
};
```

์๋ฒ์ชฝ ์ฝ๋๊ฐ ๋์ํ๋ฉด์ `open` โ `message` โ `close` ์์ ์ด๋ฒคํธ๋ฅผ ๋ณผ ์ ์๋ค.

### ์ฐธ๊ณ 

- [https://ko.javascript.info/websocket](https://ko.javascript.info/websocket)
- [http://www.secmem.org/blog/2019/08/17/websocket-socketio/](http://www.secmem.org/blog/2019/08/17/websocket-socketio/)