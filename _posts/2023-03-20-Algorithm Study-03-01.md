---
layout: single
title: 3주차 첫 번째 문제 - 터렛
---






# Baekjoon의 [터렛](https://www.acmicpc.net/problem/1002)라는 문제를 다 같이 풀어보았습니다.

<br><br><br>

## 📖 문제
![image](https://user-images.githubusercontent.com/97678547/226267249-7448a355-890d-4b42-883c-fc9c1d245df9.png)
<br><br><br>
 
## ✏️ 나의 풀이

  ```python
x0 = int(input())
location = []
for i in range(x0):
    turrets = list(map(int, input().split()))
    location.append(turrets)

for t in location:
    distance = ((t[0] - t[3])**2 + (t[1] - t[4])**2)**(1/2)
    sum_r = t[2] + t[5]
    dif_r = abs(t[2] - t[5])
    
    
    if (distance == 0) and (dif_r == 0):
        answer = -1
    elif (distance > sum_r) or (distance < dif_r):
        answer = 0
    elif (distance == sum_r) or (distance == dif_r):
        answer = 1
    elif dif_r < distance < sum_r:
        answer = 2
    
    print(answer)
  ```
  Point - 각 터렛의 위치를 원의 중심, 사거리를 반지름이라고 생각하여 두 원의 교점의 개수를 세는 문제로 이해
  1. 두 원의 중심 거리, 반지름의 합, 반지름의 차를 계산하여 각각 **distance**, **sum_r**, **dif_r**라는 변수에 할당
  2. 조건문을 활용하여 각 경우를 나누어 출력해준다.
      - 첫 번째 경우 (answer = -1)
        > - 두 원의 중심과 반지름이 동일하다면 두 원은 일치하는 원이므로 교점이 무한개가 생성된다.
      - 두 번째 경우 (answer = 0)
        > - 거리가 반지름의 합보다 큰 경우 두 원은 서로 외부에 있는 형태이다. 
        > - 거리가 반지름의 차보다 작은 경우 한 원이 다른 원을 포함하는 형태이다. 
      - 세 번째 경우 (answer = 1)
        > - 거리가 반지름의 합과 같은 경우 두 원은 서로 외접하는 형태이다.
        > - 거리가 반지름의 차와 같은 경우 두 원은 서로 내접하는 형태이다.
      - 네 번째 경우 (answer = 2)
        > - 거리가 반지름의 합보다는 작고 차보다는 큰 경우 두 원은 서로 다른 두 점에서 만나는 형태이다.
  
  <br><br><br>
  
## 💡 느낀점
  - 두 원의 교점을 구하는 문제라는 것을 이해하는데 오래 걸렸지만, 이를 이해하고 난 후에는 어렵지 않게 풀었던 것 같다.
  - 다른 스터디원들도 대부분 비슷하게 풀었던 것 같다.

<br><br><br><br>

잘못된 내용이나 피드백은 언제나 환영입니다. <br>
출처 : 백준, https://www.acmicpc.net/problemset
