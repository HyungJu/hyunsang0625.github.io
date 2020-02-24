---
title: "JavaScript 템플릿 문자열"
date: 2020-02-24 07:15:00 -0400
categories: JavaScript
---
# 템플릿 문자열
```javascript
var cart = [
    {name: '옷', price: 2000},
    {name: '가방', price: 1000}
];
var numOfItems = '카트에 ${cart.length}개의 아이템이 있습니다.'; 
var cartTable = 
`
<ul>
    <li>품목: ${cart[0].name}, 가격: ${cart[0].price}</li>
    <li>품목: ${cart[1].name}, 가격: ${cart[1].price}</li>
</ul>
`
console.log(numOfItems);
console.log(cartTable);
    
var personName = 'harin';
var helloString = 'hello' + personName;
var helloTemplateString = 'hello ${personName}';
console.log(helloString === helloTemplateString);
console.log(typeof helloTemplateString);
```
- 1~4 카트 배열을 정의한다. 카트 배열에는 name과 price를 속성으로 가지는 객체로 구성합니다.
- 5 템플릿 문자열은 억음 부호로 작성합니다. 대체로 키보드의 숫자 1 왼쪽에 위치 템플릿 문자열을 이용하면 $ {표현식}를 이용하여 삽입 처리 (interpolation)가 가능합니다.
삽입 처리란 표현식의 계산된 결과가 문자열로 변경되어 해당 위치에 삽입 되는 것 입니다.
- 6~10 템플릿 문자열은 기존 문자열과 다르게 멀티 라인이 가능합니다. 기존 문자열에서는 멀티 라인을 하기 위해 사용해야 했습니다. 템플릿 문자열은 코드 작성 시 개행하여 작성한 그대로 정의됩니다.
- 12 ~ 15 일반적인 문자열을 정의하고 두 문자열의 합한 결과를 helloString에 대입한다. helloString에는 'hello harin'이라는 값이 들어 있습니다.
- 16 ~ 18 15라인에서 두 문자열을 더했다면 helloTemplateString은 personName의 평가 결과를 삽입하도록 템플릿 문자열로 작성하였습니다. helloString과 helloTemplateString를 비교하면 두 문자열은 같은 값이고 결국엔 템플릿 문자열도 새로운 타입이 아니라 문자열인 것을 확인 할 수 있었습니다.  

```shell
카트에 ${cart.length}개의 아이템이 있습니다.    
<ul>
    <li>품목: 옷, 가격: 2000</li>
    <li>품목: 가방, 가격: 1000</li>
</ul>    
false
string
```