---
emoji: π
title: '[Javascript] attachEvent & addEventListener'
date: '2021-12-18 23:00:00'
author: μμ λ¦Ό
tags: javascript
categories: javascript
---

## κ²°λ‘  >

### `addEventListner` λ νμ€ λΈλΌμ°μ μμ μ€νλλ€. `attachEvnet` λ IE8μ΄ν λ° μ€νλΌμμ λμνλ€.

μ¬κΈ°μ νμ€ λΈλΌμ°μ λ?

- IE9, νμ΄μ΄ν­μ€, μ¬νλ¦¬, ν¬λ‘¬μ μλ―Έ

`attachEvent` μ κ²½μ°, IE11 λΆν°λ μμ ν μ κ±°λμλ€κ³  ν¨!

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
