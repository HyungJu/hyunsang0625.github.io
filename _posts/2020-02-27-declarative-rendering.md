---
title: "Vue.js 선언적 렌더링"
date: 2020-02-24 08:00:00 -0400
categories: JavaScript
---
# Vue.js 선언적 렌더링

Vue.js의 핵심에는 간단한 템플릿 구문을 사용하여 DOM에서 데이터를 선언적으로 렌더링 할 수 있는 시스템이 있습니다.

```html
<div id="app">
    {{ message }}
</div>
```
```javascript
var app = new Vue({
    el: '#app',
    data: {
        message: '안녕하세요 Vue!'
    }
})
```

이것은 문자열 템플릿을 렌더링하는 것과 매우 유사하지만, Vue.js 내부에서는 더 많은 작업을 하고 있습니다.  
데이터 DOM이 연결되었으며 모든 것이 반응형이 되었습니다. 
확인하는 방법은 브라우저의 JavaScript 콘솔을 열고 app.message를 다른 값으로 설정해 보십면 업데이트 변경된 값에 따라 업데이트가 되는 것을 볼 수 있습니다.

텍스트 보간 이외에도 다음과 같은 엘리먼트 속성을 바인딩할 수 있습니다.
```html
<div id="app-2">
  <span v-bind:title="message">
    내 위에 잠시 마우스를 올리면 동적으로 바인딩 된 title을 볼 수 있습니다!
  </span>
</div>
```
```javascript
var app2 = new Vue({
  el: '#app-2',
  data: {
    message: '이 페이지는 ' + new Date() + ' 에 로드 되었습니다'
  }
})
```
v-bind 속성은 디렉티브이라고 합니다.  
디렉티브 Vue에서 제공하는 특수 속성임을 나태는 v- 접두어가 붙어 있으며 사용자가 짐작할 수 있듯 렌더링 된 DOM에 특수한 반응형 동작을 합니다. 기본적으로 "이 요소의 **title**속성을 Vue 인스턴스의 message 속성으로 최신 상태를 유지합니다."

다시 JavaScript 콘솔을 열고 **app2.message = '새로운 메시지'** 라고 입력하면 HTML(이 경우 title 속성)이 업데이트 되었음을 다시 알 수 있습니다.