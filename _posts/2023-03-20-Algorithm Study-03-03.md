---
layout: single
title: 3주차 세 번째 문제 - 킹, 퀸, 룩, 비숍, 나이트, 폰
---






# Baekjoon의 [킹, 퀸, 룩, 비숍, 나이트, 폰](https://www.acmicpc.net/problem/3003)라는 문제를 다 같이 풀어보았습니다.

<br><br><br>

## 📖 문제
![image](https://user-images.githubusercontent.com/97678547/226271405-29cc4840-dec9-411c-bc93-fc6c1c456d68.png)
<br><br><br>
 
## ✏️ 나의 풀이

  ```python
white = list(map(int, input().split(' ')))
chess = [1, 1, 2, 2, 2, 8]
black = [i - j for i, j in zip(chess, white)]
print(*black)
  ```
  Point - 올바른 체스 피스의 개수와 가지고 있는 피스의 개수의 차를 이용
  1. 현재 가지고 있는 흰색 피스의 개수를 **white**, 올바른 체스 피스의 개수를 **chess**변수에 할당
  2. **white + black = chess** 이므로 **black = chess - white**
  3. **for반복문**과 **zip**을 활용하여 위 2번 식을 계산
  
  <br><br><br>
  
## 💡 느낀점
  - **for반복문**과 **zip**을 활용하는 기본적인 문제였다.
  - 스터디를 함께 하다보니 여러 입출력 방법을 볼 수 있었고, 
  저번에 봤던 **list comprehension**과 **print**의 리스트 앞에 * 을 붙여 리스트의 원소를 출력하는 방법을 활용하여 출력해보았다. 

<br><br><br><br>

잘못된 내용이나 피드백은 언제나 환영입니다. <br>
출처 : 백준, https://www.acmicpc.net/problemset
