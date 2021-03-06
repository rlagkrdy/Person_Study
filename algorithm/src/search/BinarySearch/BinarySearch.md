# 이진 탐색(Binary Search))

1 부터 16 까지 숫자가 있다고 가정 해보자, 이 중에서 하나의 숫자를 찾아야 한다.

일반적으로 생각을 한다면 우리는 1 부터 시작해서 찾는 숫자를 찾을 때 까지 검색을 할 것이다.

1 개를 찾는데 1 초가 걸린다고 가정하면, 1 부터 16 까지 검색하는데 총 걸리는 시간은 16 초가 걸린다.

이진 탐색은 전체를 반으로 나누어 검색을 하는 방식이다.

16 -> 8 -> 4 -> 2 -> 1

최대 4 단계 이내에 답을 구할 수 있다.

## 빅오 표기법(Big O notation)

이진 탐색을 빅오 표기법으로 표현을 하면 O(log n) 이다.

여기서 log 는 log2 이다.

1 부터 16 까지의 숫자로 계산을 한번 해보자.

log2^16 = 2 의 4 승이기 때문의 답은 4 이다.

무려 일반 검색 보다 12 초 빨라졌다.

이진 탐색의 최고의 장점은 검색 범위가 넓으면 넓을 수록 빠르다는 것이다.

이번에는 240,000 으로 계산을 다시 해보자

240k -> 120k -> 60k -> 30k -> 15k -> 7.5K -> 3750 -> 1875 ->

938 -> 269 -> 235 -> 118 -> 59 -> 30 -> 15 -> 8 -> 4 -> 2-> 1

총 18 단계 이다.

log 240000 = 18 인 것이다.

## 이진 탐색 조건

이진 탐색은 기본적으로 크다, 작다로 비교한다.

즉 숫자 타입 이거나, 숫자가 포함되어야 하며 정렬 되어 있어야 한다.

## 자바스크립트 구현 조건

1. BinarySearch 는 매개변수로 배열과 찾고자 하는 숫자를 받아야 한다.

2. 배열에 찾는 숫자가 있으면 인덱스를 리턴하고, 아니면 -1 을 리턴한다.

## 예제

1. 128 개의 이름이 정렬되어 있는 리스트가 있다. 이진 탐색으로 이름을 찾을 때
   필요한 최대의 추측 횟수는 얼마인가?

log2^128 = 7

2. 만약 리스트의 크기가 두 배가 된다면 최대 추측 횟수는 어떻게 될까?

log2^256 = 8
