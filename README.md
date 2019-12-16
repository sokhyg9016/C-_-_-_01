# C++ Primer Plus (6th Edition)
This site was built using [GitHub Pages](https://pages.github.com/).

1. **Reference**: <a href="https://isocpp.org/" target="_blank">`https://isocpp.org/`</a>
1. **Date**: 2019.12.12


## **CONTENTS**
- C++의 첫걸음 <a href="#c의-첫걸음"><sup>[1]</sup></a>
- C++ 시작하기 <a href="#c-시작하기"><sup>[2]</sup></a>

---


## C++의 첫걸음

- C와 C++언어의 역사와 철학 <a href="#c와-c언어의-역사와-철학"><sup>[1.1.1]</sup></a>
  - C의 프로그래밍 철학 <a href="#c의-프로그래밍-철학"><sup>[1.1.2]</sup></a>
  - C++의 프로그래밍 철학 <a href="#cpp의-프로그래밍-철학"><sup>[1.1.3]</sup></a>
  - 절차적 프로그래밍과 객체 지향 프로그래밍 <a href="#cpp의-프로그래밍-철학"><sup>[1.1.3]</sup></a>
  - 객체 지향 프로그래밍의 장점 <a href="#이-외의-OOP의-장점"><sup>[1.1.4]</sup></a>
- C++가 C언어에 추가한 일반화 지향 개념 <a href="#Cpp와-일반화-프로그래밍"><sup>[1.2]</sup></a>

---


C와 C++언어의 역사와 철학
---

일반적으로 컴퓨터 언어는 ***데이터***와 ***알고리즘***이라는 두가지 개념을 다룬다.

- 데이터(data): 프로그램이 사용하고 처리하는 정보
- 알고리즘(algorithm): 프로그램이 데이터를 처리하는 방법

<h4 id = "C_sec">C의 프로그래밍 철학</h4>

- `C`는 절차적(procedural)언어이다.
```   
  절차적이라는 말은 프로그래밍에서 데이터보다 알고리즘을 더 치중한다는 뜻이다. 
```
- 절차적 프로그래밍은 컴퓨터가 수행해야 할 동작들을 명확히 구분하고, 그 구분된 동작들을 프로그래밍 언어로 구현하는 것이다.
- 원하는 결과를 얻기 위해 컴퓨터가 따라야 할 절차들을 규정해 놓은 것이 `절차적 프로그램`이다.

#### 하향식(top-down)설계: 

```
- 구조적 프로그래밍이 고수하는 또 하나의 철학 
- 규모가 큰 프로그램을 작고 쉽게 다룰 수 있는 최소한의 단위로 더욱 잘게 쪼개는 것 
- 전체 프로그램이 프로그래밍하기 쉬운 작은 모듈들의 집합이 될 때까지 계속해서 쪼개 나간다. 
```

<h4 id = "Cpp_sec">Cpp의 프로그래밍 철학</h4>

- 구조적 프로그래밍 철학이 프로그램의 간결성과 신뢰성, 유지 보수의 용이성에 많은 향상을 가져온 것은 사실이나, 규모가 큰 프로그래밍은 여전히 어려운 문제로 남아 있었다. 
- 이 문제의 해결책으로 **객체 지향 프로그래밍** 철학이 등장함.

| 절차적 프로그래밍 | 객체 지향 프로그래밍 |
| --- | --- |
| `알고리즘` 강조 | `데이터` 강조 |

- 객체 지향 프로그래밍은 해결해야 할 문제를 언어의 절차적 접근 방식에 억지로 끼워 맞추지 않고, 언어 자체를 해결해야 할 문제에 맞춘다.
- **`해결해야 할 문제의 특성에 맞게 데이터형 자체를 설계한다.`**

- C++에서는 `클래스(Class)`가 그와 같은 목적으로 설계되는 새로운 데이터형이다.
- `객체(object)`는 그러한 클래스에 의해 만들어지는 특정한 데이터 구조이다.

| NOTE: OOP 환경에서는 모든 것을 `객체`로 표현하고, 이 객체의 형식을 갖는 변수를 `인스턴스(instance)`라고 한다. |
| --- |

#### 상향식(bottom-up)설계

```
- 저수준의 클래스를 먼저 설계한 후에 고수준의 프로그램 설계로 진행하는 것 
- 객체 지향적으로 프로그램을 설계하라면 프로그램이 다루는 객체를 정확하게 서술하는 클래스를 먼저 설계해야 한다. 
- 각 클래스에 해당하는 객체를 만들면서 프로그램 설계를 진행하는 것을 상향식(bottom-up)프로그래밍이라 한다.
```

| NOTE: **설계** 와 **구현** 을 분리하는 것은 OOP의 중요한 특징 중 하나이다. |
| --- |


<h4 id = "Oop_sec">이 외의 OOP의 장점</h4>

- OOP는 재활용이 가능한 소스 코드를 쉽게 작성할 수 있다. -> 프로그래밍 수고를 덜 수 있음.

***정보 은닉***
```
정보를 은닉할 수 있기 때문에 비인가된 접근으로부터 데이터를 안전하게 보호할 수 있음.
```

***다형성(polymorphism)***
```
다형성(polymorphism)을 이용하여 이름이 같은 연산자와 함수를 여러 벌 정의할 수 있기 때문에 상황에 따라 적당한 연산자나 함수를 프로그램이 스스로 선택하게 할 수 있다.
```

***상속(inheritance)***
```
상속을 이용하여 하나의 클래스로부터 새로운 클래스를 유도하는 등 절차적 프로그래밍과는 완전히 다른 접근 방식을 취할 수 있음.
```

---

Cpp와 일반화 프로그래밍
---

- 일반화 프로그래밍은 C++가 내걸고 있는 또 하나의 프로그래밍 철학이다. 
- 일반화 프로그래밍과 OOP는 소스 코드의 재활용이라는 목표와, 포괄 개념의 추상화 기술을 서로 공유한다.
- OOP는 ***`데이터`*** 를 강조하는 반면, 일반화 프로그래밍은 ***`알고리즘`*** 측면을 강조한다.

| 객체 지향 프로그래밍 | 일반화 프로그래밍 |
| --- | --- |
| **`데이터`** 를 강조 | **`알고리즘`** 를 강조 |
| 큰 프로젝트 진행시 좋음 | 데이터를 정렬(sort)하거나, 리스트를 병합(marge)하는 등의 일반적인 작업을 할 때 편리하다. |

- 여기서 `일반화(generic)`이라는 말은 **`데이터형과 무관한 코드를 작성`** 한다는 것을 의미한다.


---


## C++ 시작하기

- C++ 전처리기와 `iostream` 파일 <a href="#c-전처리기와-iostream-파일"><sup>[2.1.1]</sup></a>
- 이름 공간 (namespace) <a href="#이름-공간namespace"><sup>[2.2.1]</sup></a>
  - using 지시자 <a href="#using-지시자"><sup>[2.2.2]</sup></a>
- C++ 소스 코드 스타일 <a href="#c-소스-코드-스타일"><sup>[2.3.1]</sup></a>
  - ```cin```과 ```cout:```클래스 맛보기 <a href="#cin과-cout클래스-맛보기"><sup>[2.3.2]</sup></a>
- 함수
  - 복수 함수 프로그램에 ```using``` 지시자 넣기


---


C++ 전처리기와 `iostream` 파일
---

- C와 마찬가지로 C++도 전처리기(preprocessor)를 사용한다.
```
전처리기는 컴파일을 하기 전에 소스 파일에 대해 어떤 처리를 수행하는 프로그램이다.
```
- 전처리기는 소스 파일을 컴파일할 때 자동으로 생성된다.
- 전처리 지시자(directive)는 이름이 `#`으로 시작하는 지시자이다.

```C
#include <iostream>   //전처리 지시자
```

- `iostream`파일에는 C++의 몇 가지 입출력 기능이 정의되어 있다.
- 이 지시자는 전처리기에게 `iostream`파일의 내용을 프로그램에 추가하라고 지시한다.
- 컴파일되기 전에 소스 코드에 텍스트를 추가하거나 텍스트를 대체하는 것이 전처리기가 수행하는 기본적인 역할이다.

이름 공간(namespace)
---

- `이름 공간`은 C++의 새로운 기능이다.
- 이름 공간은 프로그램을 작성할 때 여러 소프트웨어 개발업체들이 제공하는 코드를 사용할 수 있도록 도와준다.

```Cpp
Microflop::wanda("go dancing?");  //Microflop 이름 공간의 버전
Piscine::wanda("a fish named Desire");  //Piscine 이름 공간의 버전
```
- 이러한 방식에 의해, C++ 컴파일러의 표준 구성 요소인 `클래스`, `함수`, `변수`는 `std`라는 이름 공간안에 담겨진다.
- 이와 같은 일은 `.h` 확장자가 없는 헤더 파일들 안에서 일어난다.

#### using 지시자
- 다음과 같은 행을 소스 코드에 넣으면 `std::`접두어를 붙이지 않고도 std 이름 공간에 정의되어 있는 이름들을 사용할 수 있다.

```Cpp
using namespace std;
```
- `using` 지시자는 std 이름 공간에 들어있는 모든 이름을 사용할 수 있게 해 준다.


C++ 소스 코드 스타일
---

- C++ 프로그램은 함수들의 집합이다.
- 이름 공간은 프로그램을 작성할 때 여러 소프트웨어 개발업체들이 제공하는 코드를 사용할 수 있도록 도와준다.

#### `cin`과 `cout:`클래스 맛보기
- `클래스`는 사용자가 정의하는 자료형이다.
- 클래스를 정의하려면, 클래스로 표현 할 수 있는 `정보의 종류`가 무엇이고, 그것으로 수행할 수 있는 `동작`은 무엇인지 서술해야 한다.
- 클래스와 객체의 관계는 데이터형과 변수의 관계와 같다.

|  | 클래스 | 객체 |
| --- | --- | --- |
| 정의 | 데이터 형식과 그것이 사용되는 방법을 서술하는 것 | 클래스에 서술된 형식에 따라 실제로 생성되는 구체물 |
| 예시| 유명 배우 (추상화적 개념) | 제임스 딘 (클래스가 구체화된 객체) |

- 이러한 비유를 더 확장시킨다면, `배우`라는 클래스에는 그 배우의 활동까지도 포함시킬 수 있다.
- 예를 들어, 대사 외우기, 반항아 이미지 표현하기 등등이 `배우`클래스의 동작이 될 수 있다.

| NOTE: **클래스**는 데이터 형식의 모든 속성을 서술한 것이고, **객체**는 그 서술에 따라 실제로 생성된 구체물이다. |
| --- |

- 이제 `cout`을 살펴보자면,

> **iostream**

```Cpp
...
__PURE_APPDOMAIN_GLOBAL extern _CRTDATA2_IMPORT istream cin, *_Ptr_cin;
__PURE_APPDOMAIN_GLOBAL extern _CRTDATA2_IMPORT ostream cout, *_Ptr_cout;
...
```
- `cout`은 `ostream`클래스의 속성을 가지고 생성된 객체이다.
- `ostream`클래스는 `iostream`파일에 정의되어 있다.
- `ostream`클래스 정의에는 ostream 객체가 표현할 수 있는 데이터 형식이나, 그 데이터 형식을 가지고 수행할 수 있는 동작, 예를 들어 문자열을 출력 스트림에 삽입하는 동작 등을 정의하고 있다.
- 마찬가지로 `cin`은 `istream`클래스의 속성을 가지고 생성된 객체이며, 이것 역시 `iostream` 파일에 정의되어 있다.

| NOTE: 주의해야 할 점은 `cin`은 C언어의 `scanf("%s", str);`와 같이 문자열을 공백문자로 구분하기 때문에 문자열 추출 시 항상 구문(phrase)나 전체 문장(sentence)가 아닌 하나의 단어(word)를 추출한다. |
| --- |

- 따라서 `cin`으로부터 전체 문장을 받기 위해서는 `getline`함수를 사용한다.

```Cpp
//C++ 11
istream& getline (istream&  is, string& str, char delim);
istream& getline (istream&& is, string& str, char delim);	
istream& getline (istream&  is, string& str);
istream& getline (istream&& is, string& str);

/*
is: istream object from which characters are extracted.
str: string object where the extracted line is stored.
     The contents in the string before the call (if any) are discarded and replaced by the extracted line.
     
Return value: The same as parameter is.
*/

//Example 

// extract to string
#include <iostream>
#include <string>

int main ()
{
  std::string name;

  std::cout << "Please, enter your full name: ";
  std::getline (std::cin, name);
  std::cout << "Hello, " << name << "!\n";

  return 0;
}
```
- Get line from stream into string.
- Extract characters from `is` and stores them into `str` until the delimitation character `delim` is found. (or the new line, `\n`).
