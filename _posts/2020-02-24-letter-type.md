---
title: "JavaScript 문자형"
date: 2020-02-24 04:45 :00 -0400
categories: JavaScript
---
# 017. 문자형 이해하기
**문자형(String)** 은 값이 텍스트 형태인 데이터를 의미한다.
```javascript
console.log('I m in Jeju');
console.log('Sewha ocean is wonderful');
console.log('Have you ever eaten Makgeolli?');
console.log('This is the first line\nAnd this is the second');
```
```
I m in Jeju
Sewha ocean is wonderful
Have you ever eaten Makgeolli?
This is the first line
And this is the second
```
- 큰 따움표로 작성된 I m in Jeju 문자열을 출력합니다.
- 작은 따움표로 작성된 Sewha ocean is wonderful 문자열을 출력합니다.
- 억음 부호로 Have you ever eaten Makgeolli? 문자열을 출력합니다.
- 개행이 있는 This is the first line\nAnd this is the second 문장을 출력하면, This is the first line
이후에 다음 문장으로 넘아가 And this is the second이 출력됩니다.

문자열로 표현할 때는 큰따움표("), 작은따움표('), 억음 부호(`)와 함께 사용합니다.  
처음과 끝에 기호로 둘러싸인 형태로 문자열로 작성되며, 처음과 끝의 기호는 동일해야 합니다.  

다른 언어와 달리 자바스크립트는 큰따옴표 문자열과 작은따움표 문자열 간의 차이점은 없다, 따음표 기호들은 단일 문장이어야 유효하나, 간혹 개형이 필요한 문장도 있습니다.  
따음표로 묶인 텍스트 안에  **\n**을 추가하면 개행이 가능합니다.  
백슬래시 뒤의 문자는 경우에 따라 변경할 수 있습니다.  