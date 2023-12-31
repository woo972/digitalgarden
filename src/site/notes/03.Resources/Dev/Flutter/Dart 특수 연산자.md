---
{"dg-publish":true,"permalink":"/03.Resources/Dev/Flutter/Dart 특수 연산자/","tags":["dart","dev"],"noteIcon":""}
---


1. spread 표기법 : multiple elements를 collection으로 변경하는 역할

```jsx
// ... 연산자
var list_a = [1,2,3];
var list_b = [4, ... list_a];  // list_b.length == 4

// ...? 연산자 
// (collection으로 변경하려는 elements가 null이 의심될 때 사용)
var list_a;
var list_b = [4, ...? list_b]; // list_b.length ==4
```

[https://stackoverflow.com/questions/57194452/meaning-of-triple-dots-in-flutter-syntax/57195798](https://stackoverflow.com/questions/57194452/meaning-of-triple-dots-in-flutter-syntax/57195798)

2. cascade 표기법 :  this 대체

```dart
// 사용법 예1
List list1 = List()..add(1)..add(2);
(불가능한 표현법: List list1 = List().add(1).add(2));

// 사용법 예2
List list2=[];
list2..add(1)..add(2);
```

[https://stackoverflow.com/questions/49447736/list-use-of-double-dot-in-dart](https://stackoverflow.com/questions/49447736/list-use-of-double-dot-in-dart)`

3. null aware 표기법: isnull 대체

```jsx
// 사용법 예1
// x에 값 대입 - y가 null 이면 z
x = y??z   

// 사용법 예2
// x가 null 이면 y 대입
x??=y

// 사용법 예3
// x가 notnull 이면 method 호출
x?.abc()
```

[http://blog.sethladd.com/2015/07/null-aware-operators-in-dart.html](http://blog.sethladd.com/2015/07/null-aware-operators-in-dart.html)