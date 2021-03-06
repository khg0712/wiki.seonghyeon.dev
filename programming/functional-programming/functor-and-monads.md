# Functor and Monads

## Functor

* 감싸진 값에 함수를 적용하는 방법
* Future, List, Maybe에 있는 map: 감싸져있는 값에 함수를 적용하게 해주는 펑터를 구현한 것

## Monads

* 감싸진 값을 리턴하는 함수에 감싸진 값을 밀어넣는 방법
    * 모나드가 되려면...
        * 타입 생성자가 있어야 한다
        * 모나드가 아닌 값을 받아 모나드를 리턴하는 함수에 모나드로 감싸진 값을 집어넣는 바인드를 지원해야 한다
        * 모나드로 다른 타입을 감싸는 것을 지원해야 한다.
    * 위 특성(타입클래스/인터페이스)들을 만족한다면 그것은 모나드다 
* ROP에서 `T -> Result U` 의 시그니처를 가지는 함수들을 `Result T -> Result U` 로 바꿔서 체이닝 해주는것도 모나드의 개념
    * Maybe(Optional) 같은 타입들도 모나드기 때문에 `>>=`처럼 바인드를 지원 
