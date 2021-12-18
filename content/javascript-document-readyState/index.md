---
emoji: ☃️
title: '[Javascript] document.readyState'
date: '2021-12-18 23:00:00'
author: 서유림
tags: javascript
categories: javascript 
---

### `Document.readyState` 속성을 통해 document의 로딩 상태를 확인할 수 있다.

- document.readyState 속성 값이 바뀔 때 `readystatechange` 이벤트다 document에서 일어난다.

### Syntax

```jsx
var isReady = document.readyState;
```

### Values

1. `loading`
    1.  document 로딩 중
2. `interactive`
    1. 문서의 로딩은 끝이 나고 해석 중 이지만 images, stylesheets, frames과 같은 하위 자원들은 로딩되고 있는 상태
3. `complete`
    1. 문서와 모든 하위 자원들의 로드가 완료된 상태.