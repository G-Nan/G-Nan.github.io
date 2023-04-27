---
layout: single
title: 5주차  첫 번째 문제 - 당구 연습
---





<br>

# Programmers의 [당구 연습](https://school.programmers.co.kr/learn/courses/30/lessons/169198)라는 문제를 다 같이 풀어보았습니다.

<br><br><br>

## 📖 문제
![image](https://user-images.githubusercontent.com/97678547/234786509-14ff2d28-439f-4eb1-9983-cb47b3f25dc1.png)

<br><br><br>
 
## ✏️ 나의 풀이

  ```python
def solution(m, n, startX, startY, balls):
    answer = []
    loc = []


    for ball in balls:
        a, b, c, d = startX, startY, ball[0], ball[1]
        left = (a+c)**2+(b-d)**2
        right = (2*m-(a+c))**2+(b-d)**2
        bottom = (a-c)**2+(b+d)**2
        top = (a-c)**2+(2*n-(b+d))**2
        dis = [left, right, bottom, top]
        
        if startX == ball[0]:
            if startY > ball[1]:
                del dis[2]
            elif startY < ball[1]:
                del dis[3]
        elif startY == ball[1]:
            if startX > ball[0]:
                del dis[0]
            elif startX < ball[0]:
                del dis[1]
        
        answer.append(min(dis))
    return answer
  ```
  Point - 공을 쳐서 부딪히는 벽 4방향의 상황을 모두 고려하여 거리를 계산한 후 최소값을 산출
  1. **for문**을 이용하여 쳐야하는 공의 위치의 **x좌표**, **y좌표**, 목표 공의 **x좌표**, **y좌표**를 각각 **a**, **b**, **c**, **d**에 넣어줌. 
  2. 각 벽에 부딪히는 경우의 거리구하는 식을 계산한 후 **dis**변수에 넣어줌.
      ex) 왼쪽 벽에 부딪히는 경우 **left**, 아래쪽 벽에 부딪히는 경우 **bottom**
  3. 치는 공과 목표 공의 **x좌표 or y좌표**가 같은 경우는 예외처리를 하여 계산.
  4. 이후 나올 수 있는 거리의 최솟값을 산출


  <br><br><br>
  
## 💡 느낀점
  - 거리를 구하고 최솟값을 구하는 방법은 어렵지 않았지만, 예외처리를 하는 부분에서 자꾸 실수가 나서 오래걸린 문제였다.

<br><br><br><br>

잘못된 내용이나 피드백은 언제나 환영입니다. <br>
출처 : 프로그래머스 코딩 테스트 연습, https://school.programmers.co.kr/learn/challenges
