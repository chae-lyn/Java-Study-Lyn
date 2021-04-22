제어문(Control Statement)
====

## 조건문
### if
- 주어진 조건식이 true이면 값을 산출, false면 실행하지 않음

```java
int num = 50;
if(num <=50){
    System.out.println("50보다 작거나 같습니다!");
    // if 조건식이 참인것만 출력됨
}
if(num > 50){
    System.out.println("50보다 큽니다!");
    // if 조건식이 거짓이여서 출력되지 않음
}
```

### if else
- 조건이 true일 경우 if가 실행되고 false일 경우 else가 실행됨
``` java
int num = 50;

if(num % 2 == 0) {
System.out.println("짝수");
} else {
System.out.println("홀수");
}
// => 짝수 출력됨
```

### switch
- 변수의 값에 따라 결과값이 결정됨
```java
int num = 3;
switch(num){
    case 1:
        System.out.println("1번입니다 !");
        break;
    case 1:
        System.out.println("2번입니다 !");
        break;
    case 1:
        System.out.println("3번입니다 !");
        break;
}
// => 3번 출력됨
```

## 반복문
- 특정한 조건식을 걸어주면 정해진 횟수나 값이 true가 나올때까지 반복을 하는 개념

### for 
- 반복문내에 조건식이 true일 경우 증감식을 통한 실행문을 따라 계속 반복하다가, 증감식이 false가 되면 for문이 종료

```
for(초기식; 조건식; 증감식) {
수행될 문장;
}
```   

```java  
for(int i = 1; i <= 10; i++) {
System.out.print(i + “ 출력");
}
/* 
=>    1출력 
      2출력 
      ... 
      9출력 
      10출력
*/
```   

### while
- 조건식이 true일 경우 계속 반복함
```
while(조건식) {
수행될 문장;
[증감식 or 분기문];
}
```

```java
int i = 1;
while(i <= 10) {
System.out.println(i + " 출력");
i++;
}
/* 
=>    1출력 
      2출력 
      ... 
      9출력 
      10출력
*/
```
### do ~ while
- do 안의 내용 먼저 실행 조건식 확인 후 true면 문장 수행, false면 종료되며 while 뒤에 ; 꼭 필요
```
do {
수행될 문장;
[증감식 or 분기문];
} while(조건식);
```
```java
int i = 1;
do {
System.out.println(i + "출력");
i++;
} while(i <= 10);
/* 
=>    1출력 
      2출력 
      ... 
      9출력 
      10출력
*/
```
### while과 do~while의 차이점
- do~while은 조건문이 true가 아니더라도 무조건 한 번 이상 수행

## 분기문
### break 
- 반복문에서 break문은 자신이 포함된 가장 가까운 반복문을 빠져나가는 구문
```java
for(int i = 1; ; i++) {
    System.out.println(i + " 출력");
    if(i >= 10) {
        break;
        // i 가 10이상이면 반복문 종료됨
    }
}
```
### continue
- 반복문 내에서만 사용가능, 반복문 실행시 continue 아래 부분은 실행하지 않고 반복문 다시 실행
    + for문의 경우 증감식으로 이동
    + while(do ~ while)문의 경우 조건식으로 이동
    + 전체 반복중에 특정조건을 만족하는 경우를 제외하고자 할 때 유용

```java
for(int i = 1; i <= 10; i++) {
    if(i % 2 == 0) {
        continue;
    }
    System.out.println(i + " 출력");
}
/*
=> 1 출력
   3 출력
   5 출력
   7 출력
   9 출력
*/
```