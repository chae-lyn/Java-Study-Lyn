객체(Object)
====

## 객체지향언어
- 사물이나 개념처럼 독립되고 구분되는 각각의 객체로 이루어져 있으며 발생하는 모든 사건들은 객체간의 상호작용
- 현실에서의 객체 : 독립적으로 존재하는 것들 (유형,무형,개념 ...)
- 자바에서의 객체 : 클래스에 정의된 내용대로 new 연산자를 통해 메모리 영역에 생성된 것

- 장점 : 재사용성, 생산성향상, 자연적인 모델링, 유지보수의 우수성
- 단점 : 개발속도, 실행속도가 느려짐, 코딩난이도 상승

## 캡슐화(Encapsulation)
- 데이터와 코드의 형태를 외부로부터 알 수 없게 하고 데이터의 구조와 역할, 기능을 하나의 캡슐형태로 만드는 방법

## 상속(Inheritance)
- 상위 클래스의 모든걸 하위 클래스가 모두 이어받는 것

## 다형성(Polymorphism)
- 상속과 연관이 있는 개렴으로 한 객체가 다른 여러형태(객체)로 재구성되는 것

## 추상화(abstraction)
- 객체의 공통적인 속성과 기능을 추출하여 정의하는 것

## 클래스(class)
- 객체의 특성(속성, 기능)에 대한 정의
```
[접근제한자] [예약어] class 클래스명 {

[접근제한자] [예약어] 자료형 변수명;
[접근제한자] [예약어] 자료형 변수명;

[접근제한자] 생성자명() { } 

[접근제한자] 반환형 메소드명(매개변수) {    
    // 기능 정의
    }
}
```   
```java
// 클래스 예시
public class Member{
    private String name;
    private int age;
<<<<<<< HEAD

=======
 
>>>>>>> study
    public Member(){}

    public String getName(){
        return name;
    }
    public void setName(String name) {
        this.name = name;
    }
    public int getAge() {
        return age;
    }
    public void setAge(int age) {
        this.age = age;
}
```

### 접근제한자

|구분|   | 같은 패키지 내 | 전체 |
|:---|:---|:---:|:---:|
| + | public | O | O |
| ~ | (default) | O | O |

## 필드(Field)
```
[접근제한자] [예약어] class 클래스명 {
    [접근제한자] [예약어] 자료형 변수명 [= 초기값];
}
```   
```java
public class Academy { 
    public int temp1;
    protected int temp2;
    int temp3; // 접근제한자 생략 시 default
    private int temp4; // 캡슐화 원칙으로 private 사용
}
```

### 필드 접근제한자
|구분|   | 해당 클래스 내부 | 같은 패키지 내 | 후손 클래스 내 | 전체 |
|:---|:---|:---:|:---:|:---:|:---:|
| + | public | O | O | O | O |
| # | protected | O | O | O | |
| ~ | (default) | O | O |  | |
| - | private | O |  |  | |

### 필드 예약어
- static
    + 같은 타입의 여러객체가 공유할 목적의 필드에 사용
    + 프로그램 시작시 정적 메모리 영역에 자동 할당되는 멤버에 적용
- final
    + 하나의 값만 계속 저장해야 하는 변수에 사용

```java
// static 표현식
public class Academy{
    private static int num1;
}

// final 표현식
public class Academy{
    private final int num1 = 10;
    private int num2;
}
```

### 클래스 초기화 블럭
- 인스턴스 블럭
    + {}  
    + 인스턴스 변수를 초기화시키는 블럭, 객체 생성시마다 초기화
- static(클래스) 블럭
    + static{}   
    + static 필드를 초기화 시키는 블럭으로 프로그램 시작시 한번만 초기화
```
[접근제한자] [예약어] class 클래스명 {
    [접근제한자] static 자료형 필드1;
    [접근제한자] 자료형 필드2;

    static{ 필드1 = 초기값; }
<<<<<<< HEAD
    
=======

>>>>>>> study
    { 필드2 = 초기값; }
}
```

### 필드 초기화 순서
```
// 클래스 변수
JVN 기본값 -> 명시적 초기값 -> 클래스 초기화 블록 초기값

// 인스턴스 변수
JVN 기본값 -> 명시적 초기값 -> 인스턴스 초기화 블록 초기값 -> 생성자를 통한 초기값
```