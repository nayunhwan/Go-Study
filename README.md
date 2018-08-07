# Go 언어의 특징

- 컴파일 언어
- 강타입 언어, 컴파일러가 타입 추론 지원
- 가비지 컬렉션
- 클로져 (Closure)
- 고루틴 (Goroutine: 경량화 스레드)
- 채널 (Channel: Goroutine 간 데이터 교환 방법)
- 빠른 컴파일 속도
- Cgo(C 코드 사용)
- 현대화된 라이브러리 (Battery-included standard libraries)
  - (Javascript 는 Dependency 가 높은 라이브러리가 있지만, GoLang 은 이미 Standard Library 에 포함되어 있어, 굳이 사용할 필요가 없고, 또한 사용하더라도, Dependency 가 높지 않다.)
- 크로스 컴파일 기본 지원 (Windows 로 개발하다 Mac 용으로 바꾸기 쉽다.)
- 다양한 도구 제공 (`fmt`, `vet`, `fix`, `get`, `install` 등)

## First impression

```go
package main

import "fmt"

func main() {
    fmt.Println("Hello, World!")
    fmt.Println("안녕, 세상아!")

    이름 := "Naver D2 Campus Seminar" /* 타입을 추론한다. */

    fmt.Printf("안녕, %s\n", 이름);
}
```

## Type System

- numeric
- string
- **function**
- **struct** (Go 언어의 객체 타입)
- **interface**
- **array** (Fixed Length) & **slice** (Dynamic Length)
- pointer
- **map** (python 의 Dictionary 와 비슷하다)
- **channel**

## Variable

### Declair Variable

```go
var a int = 10
var b string = "hello, world"
var c bool  /* false 초기화*/
```

### Short Declair variable

```go
d := 1.0  /* float */
e := true /* boolean */
f := "Hello, world" /* string */
```

## 제어문

## 다중 리턴

## struct

- Go 언어의 객체
- 대문자로 시작하는 필드는 **Public** 소문자로 시작하면, **Private**

## interface 타입

- Duck typing: 인터페이스를 구현한다는 명시적인 선언이 없음

## Error Type

```go
func Open(name string) (*File, error) /* 보통 Error를 같이 Return한다 Try catch 대체 */
```

## 통신(Communicating)하여 메모리를 공유

메모리를 공유해서 통신하지 말고, 통신하여 메모리를 공유합시다.

## ex

https://go-tour-kr.appspot.com/
