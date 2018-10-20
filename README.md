# Haskell

## 특징
- 함수형 프로그래밍 언어로 참조 효과가 없기 때문에 부작용이 없다.
- 정적 타입 언어이다.
- 좋은 형식 유추를 사용하기 때문에 변수 선언 시 하스켈이 자체적으로
  알아낼 수 있는 유형의 레이블을 지정할 필요가 없다.
- 함수 이름, 공백을 입력한 다음 인자를 공백으로 구분하여 씀으로써 함수를
  호출할 수 있다.
- 인자를 괄호로 묶음으로써 우선순위를 높일 수 있다.
- 함수 이름을 backtick(\`)으로 묶고 중위 표기법을 사용하여 함수를 호출할
  수 있다.
```hs
$ add x y = x + y
$ 3 `add` 4
# 7
```
- if 문은 또다른 표현식일 뿐이며, else는 반드시 후행되어야 한다.
- 함수는 소문자로 시작되어야 한다.
- 리스트는 동질적인 데이터 구조로 단일 리스트에 다른 유형의 요소를 사용할 수 없다.
- `++` 연산자를 통해 리스트에 리스트를 추가할 수 있다.
```hs
$ [1, 2, 3] ++ [4, 5, 6]
# [1, 2, 3, 4, 5, 6]
```
- `:`를 사용하여 리스트의 시작 부분에 요소를 추가할 수 있다.
```hs
$ 0 : [1, 2, 3]
# [0, 1, 2, 3]
```
- `!!`를 사용하여 리스트에서 요소를 가져올 수 있다.
```hs
$ [1, 2, 3, 4, 5] !! 3
# 4
```
- 리스트는 비교될 수 있다.

## Functions for List
__head__
```hs
-- take a list and return its first element

head [1, 2, 3, 4, 5]
-- Output : 1
```

__tail__
```hs
-- take a list and return its every elements except the head

tail [1, 2, 3, 4, 5]
-- Output : [2, 3, 4, 5]
```

__last__
```hs
-- take a list and return its last element

last [1, 2, 3, 4, 5]
-- Output : 5
```

__init__
```hs
-- take a list and return its every elements except the last

init [1, 2, 3, 4, 5]
-- Output : [1, 2, 3, 4]
```

__length__
```hs
-- take a list and return its length

length [1, 2, 3, 4, 5]
-- Output : 5
```

__null__
```hs
-- take a element and a list and tell whether the list is empty

null [1, 2, 3, 4, 5]
-- Output: False

null []
-- Output: True
```

__reverse__
```hs
-- take a list and return the reversed list

reverse [1, 2, 3, 4, 5]
-- Output: [5, 4, 3, 2, 1]
```

__take__
```hs
-- take a number as an index and a list. then return the first n elements in the list

take 3 [1, 2, 3, 4, 5]
-- Output: [1, 2, 3]
```

__drop__
```hs
-- take a number as an index and a list. then return the list without first that elements

drop 3 [1, 2, 3, 4, 5]
-- Output: [4, 5]
```

__maximum__
```hs
-- take a list and return the biggest element

maximu [1, 2, 3, 4, 5]
-- Output: 5
```

__minumum__
```hs
-- take a list and return the smallest element

minimum [1, 2, 3, 4, 5]
-- Output: 1
```

__sum__
```hs
-- take a list and return the sum of elements in list

sum [1, 2, 3, 4, 5]
-- Output: 15
```

__product__
```hs
-- take a list and return the product of elements in list

sum [1, 2, 3, 4, 5]
-- Output: 120
```

__elem__
```hs
-- take a element and a list and tell whether the element exist in the list

elem 0 [1, 2, 3, 4, 5]
-- Output: False

elem 2 [1, 2, 3, 4, 5]
-- Output: True
```

__range__
```hs
[1 .. 5]
-- Output: [1, 2, 3, 4, 5]

[1, 1.5 .. 5]
-- Ouput: [1.0, 1.5, 2.0, 2.5, 3.0, 3.5, 4.0, 4.5, 5.0]

[1, 4 .. 5]
-- Output: [1, 4]
```

## Installation
```
$ brew install haskell-stack
$ stack setup
$ stack ghci
```

## Exit from GHCI
- `Ctrl + D`
