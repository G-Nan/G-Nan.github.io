---
layout: single
title: 4주차 첫 번째 문제 - 평균은 넘겠지
---





<br>

# Baekjoon의 [평균은 넘겠지](https://www.acmicpc.net/problem/4344)라는 문제를 다 같이 풀어보았습니다.

<br><br><br>

## 📖 문제
![image](https://user-images.githubusercontent.com/97678547/229465830-77af52a7-b8b5-43fc-ba3a-0c5ea1321ecc.png)
<br><br><br>
 
## ✏️ 나의 풀이

  ```python
x0 = int(input())
x = [list(map(int, input().split( ))) for _ in range(x0)]

for i in x:
    k = 0
    mean = sum(i[1:])/i[0]
    for j in i[1:]:
        if j > mean:
            k += 1
    smart = (k/i[0])*100
    print('%0.3f' %smart  + '%')
  ```
  Point - 평균을 구한 후 평균을 넘은 사람 수를 구하고 비율을 계산
  1. 평균을 구하여 **mean** 변수에 할당
  2. 반복문을 이용해 각 학생의 점수가 평균을 넘을 때 마다 **k**에 1씩 더해줘 평균을 넘는 학생 수를 계산
  3. 평균을 넘는 학생 수 / 전체 학생 수를 계산하여 **smart** 변수에 할당
  4. 소수점 셋째 자리까지 출력



  <br><br><br>
  
## 💡 느낀점
  - **반복문**을 이용하는 기본적인 문제였다.
  - 딱히 어려움 없이 풀었던 것 같다.

<br><br><br><br>

잘못된 내용이나 피드백은 언제나 환영입니다. <br>
출처 : 백준, https://www.acmicpc.net/problemset
