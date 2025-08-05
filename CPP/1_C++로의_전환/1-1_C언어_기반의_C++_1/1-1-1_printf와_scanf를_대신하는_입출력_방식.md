# printf와 scanf를 대신하는 입출력 방식

C++도 "Hello world" 출력 예제로 시작한다. </br>
C 버전과 조금 다르지만, 초보자는 먼저 눈에 익히고 외우는 과정이 정상적이다.

"Hello World"를 출력하는 예제를 실행해 보자.
> [1_Hello_World.cpp](1_Hello_World.cpp)
```cpp
#include <iostream>

int main()
{
    int num = 20;
    std::cout << "Hello World!" << std::endl;
    std::cout << "Hello " << "World!" << std::endl;
    std::cout << num << ' ' << 'A';
    std::cout << ' ' << 3.14 << std::endl;
    
    return 0;
}
```
C++ 파일은 확장자를 .cpp로 지정해야 C++ 문법 규칙이 적용된다.

출력 관련 특징:
* #include <iostream> 헤더 사용
* std::cout과 << 연산자를 이용한 출력
* std::endl을 이용한 개행

