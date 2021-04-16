DataType, Variable, Array
===

데이터 타입 (DataType)
===
- 프로그래밍 언어에서 사용할 수 있는 데이터의 종류
- 기본 데이터형(primitive)과 참조 데이터형(reference)으로 나뉨

기본 데이터형(primitive)
====
- 총 8가지의 기본형 타입을 미리 정의하여 제공
- 기본값이 있어 Null이 존재하지 않음

|    | 타입 | 메모리 크기 | 기본값 | 데이터의 표현 범위 |
|:---|:---|:---:|:---:|---:|
| 논리형 | boolean | 1byte | false | true, false |
| 정수형 | byte | 1byte | 0 | -128 ~ 127 |
|       | short | byte | 0 | -32,768 ~ 32,767 |
|       | int   | 4byte | 0 | -2,147,483,648 ~ 2,147,483,647 |
|       | lont  | 8byte | 0 | -9,223,372,036,854,775,808 ~ 9,223,372,036,854,775,807 |
| 실수형 | float | 4byte | 0.0F | 1.4E-45 ~ 3.4028235E38 |
|       | double | 8byte | 0 | 4.9E-324 ~ 1.7976931348623157E308 |
|   | 문자형 | char | 2byte | '\u0000' | 0 ~ 65,535 |

참조 데이터형(reference)
====
- 기본형 타입을 제외한 타입들
- 빈 객체를 의미하는 Null이 존재

|   | 타입 | 예시 | 기본값 | 할당되는 메모리 크기 |
|:---|:---|:---:|:---:|---:|
|   | 배열(Array) | ```java int[] arr = new int[5];```| Null | 4byte |
|   | 열거(Enumeration) |   | Null | 4byte |
|   | 클래스(class) | ```java String str= "test"; \n Student s = new Student();``` | Null | 4byte |
|   | 인터페이스(Interface) |   | Null | 4byte |