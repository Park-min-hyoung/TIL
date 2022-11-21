<!-- 작성 샘플 -->

# 6월 7일

## 오늘 한일

### `면접 준비`

- 데상트 코리아 면접 준비
- 면접 질문 리스트 정리 및 답변 작성

<br>

## 배운 것

<br>

## 어려웠던 점

<br>

## 한줄평

> _이번주도 수고했어!!! 내일부터 코테랑 면접 준비 잘하자!!!_

<br>

<!-- 문제 출처 -->

> 블로그 자료

- [구글, "JS 모듈 시스템과 순환 참조 문제", https://ljs0705.medium.com/js-모듈-시스템과-순환-참조-문제-a9e0c90c07e5, (2022.07.07)]

[구글, "js 모듈 시스템과 순환 참조 문제", https://ljs0705.medium.com/js-모듈-시스템과-순환-참조-문제-a9e0c90c07e5, (2022.07.07)]: https://programmers.co.kr/learn/courses/30/lessons/59410

> 인터넷 검색

- [사이트명, "검색어", URL, (참고 날짜)
  ex) 네이버, "허성진", https://www.naver.com, (2021.10.25)]

- [사이트명, "검색어", url, (참고 날짜) ex) 네이버, "허성진", https://www.naver.com, (2021.10.25)]: https://programmers.co.kr/learn/courses/30/lessons/59410

<!-- 제목 목록 -->

### `이력서 작성`

### `ES6 강의`

### `CRUD 게시판 제작`

### `코딩테스트: 파이썬 개념`

### `코딩 테스트`

- 파이썬 알고리즘 인터뷰 책 읽기
- leetcode 문제 `문자열 조작` => 5. 가장 긴 팰린드롬 부분 문자열
- 백준 단계별로 풀어보기 `정렬` => 통계학
- 알고리즘 기초 Part 2 `자료구조 1`, `자료구조 1(연습)`문제 풀이
- `에디터`, `단어 뒤집기 2` 해설, `쇠막대기` 풀이

### `ES6 부족한 개념 보완`

### `Netflix 클론코딩`

### `React 강의`

### `스포츠 용병 서비스 팀플`

### `프론트엔드 데브코스`

- core time 참석
- 데일리 스크럼
- js 강의 수강
- 과제 수행 중
- 로토님 특강
- 노마드 코더 React 강의 수강

### `프론트엔드 데브코스`

<br>

#### `js 강의`

<br>

### `TIL 복습`

- 이번주 TIL 읽기

### 출처

- https://velog.io/@lucasheo/블로그-저작권과-출처-표기

### `코딩테스트`

<br>

#### 백준 `후위 표기식2`

```py
import sys

n = int(sys.stdin.readline())
data = list(sys.stdin.readline().rstrip())
number = list(int(sys.stdin.readline().rstrip()) for _ in range(n))

stack = []
for item in data:
    if "A" <= item <= "Z":
        stack.append(number[ord(item) - ord('A')])
    else:
        back = stack.pop()
        front = stack.pop()
        if item == '*':
            stack.append(front * back)
        elif item == '+':
            stack.append(front + back)
        elif item == '/':
            stack.append(front / back)
        else:
            stack.append(front - back)
print("%.2f" %stack[-1])
```

> 풀이

1. 알파벳 모양의 피연산자를 숫자로 바꾸어 stack에 넣기
   - number = [3, 5, 8]
   - 3개의 피 연산자 값이 주어졌다면, A => 0번 index, B => 1번 index, C => 2번 index
   - number[ord(알파벳) - ord('A')]를 이용해 index 구한 후 숫자 값을 stack에 append
2. 연산자는 stack에서 item 2개를 꺼내어 연산 후 결과를 다시 stack append

> 출처

- [백준 후위 표기식2 문제 출처]
- [후위 표기식2 해설 출처]

[백준 후위 표기식2 문제 출처]: https://www.acmicpc.net/problem/1935
[후위 표기식2 해설 출처]: https://www.acmicpc.net/problem/1935
