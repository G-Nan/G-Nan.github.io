---
layout: single
title: 2주차 두 번째 문제 - 달팽이는 올라가고 싶다
---






# Baekjoon의 [달팽이는 올라가고 싶다](https://www.acmicpc.net/problem/2869)라는 문제를 다 같이 풀어보았습니다.

<br><br><br>

 ## 📖 문제
 
![image](https://user-images.githubusercontent.com/97678547/223656299-5d586878-f366-41a0-8cd1-2c2d09043477.png)
 <br><br><br>
 
 ## ✏️ 나의 풀이

  ```python
import math

A, B, V = map(int, input().split( ))
answer = 0

V -= A
answer += 1

up = A - B
answer += math.ceil(V / up)

print(answer)
  ```
  Point - 나무 막대를 모두 올라가는 순간은 무조건 낮에 발생 <br>
  　　　  그렇기에 막대를 올라간 후 내려온다고 생각하는 것이 아니라 내려온 후 올라간다고 생각
  1. 막대의 높이 **V**에서 **A**만큼 먼저 올라간 후 1일이 지난 것으로 판단하여 **answer**에 1을 더해줌
  2. 하루에 내려오고 올라가는 정도를 **up**이라는 변수에 할당
  3. 남은 막대의 높이 **V**를 하루에 **up** 만큼 가는 것이기에 **V**를 **up**으로 나눠준 후 소수 첫째 자리에서 올림 <br>
  ex) 높이가 7, 하루에 2씩 올라간다 가정하면 7을 2로 나눈 값 3.5에서 소수 첫째 자리에서 올림을 해주면 4라는 답이 나온다.
  <br><br><br>
  
 ## 💡 느낀점
 
  - 다른 스터디원들은 여러가지 경우를 나누어 반복문을 사용하였는데, 이 경우 시간초과가 되었다고 한다.
  - 대학 전공에서 배운 해석학이나 정수론이 이럴 때는 확실히 도움이 되는 것 같다.
      
<br><br><br><br>

잘못된 내용이나 피드백은 언제나 환영입니다. <br>
출처 : 백준, https://www.acmicpc.net/problemset
