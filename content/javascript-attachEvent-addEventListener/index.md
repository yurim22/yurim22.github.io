---
emoji: 🌈
title: '[Javascript] attachEvent & addEventListener'
date: '2021-12-18 23:00:00'
author: 서유림
tags: javascript
categories: javascript
---

## 결론 >

### `addEventListner` 는 표준 브라우저에서 실행된다. `attachEvnet` 는 IE8이하 및 오페라에서 동작한다.

여기서 표준 브라우저란?

- IE9, 파이어폭스, 사파리, 크롬을 의미

`attachEvent` 의 경우, IE11 부터는 완전히 제거되었다고 함!

```javascript
var t = document.getElementById('target');

if (t.addEventListener) {
  t.addEventListener('click', function (event) {
    alert('Hello world, ' + event.target.value);
  });
} else if (t.attachEvent) {
  t.attachEvent('onClick', function (event) {
    alert('Hello world, ' + event.target.value);
  });
}
```

```javascript
function AddEvent(a, b) {
  var div = document.getElementById('div');

  if (div.addEventListener) {
    div.addEventListener(
      'click',
      function (a, b) {
        test(a, b);
      },
      false,
    );
  } else {
    div.attachEvent('onclick', function (a, b) {
      test(a, b);
    });
  }
}

function test(a, b) {
  alert(a + b);
}
```
