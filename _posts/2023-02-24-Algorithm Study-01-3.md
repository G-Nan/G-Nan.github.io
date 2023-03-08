---
layout: single
title: 1주차 세 번째 문제 - 푸드 파이트 대회
---






# Programmers의 [푸드 파이트 대회](https://school.programmers.co.kr/learn/courses/30/lessons/134240)라는 문제를 다 같이 풀어보았습니다.

<br><br><br>

## 📖 문제
 ![image](https://user-images.githubusercontent.com/97678547/221114200-3bd90e26-d59a-4059-a7a1-c1b3d69a79b0.png)
 <br><br><br>
 
## ✏️ 나의 풀이

```python
def solution(food):
   answer = ''
   
   k = 0
   eat = ''
   for i in food: 
       if k == 0:
           pass
       
       eat += str(k) * (i // 2)
       k += 1
   
   answer = eat + '0' + eat[::-1]
   return answer
  ```
  1. **food**의 가장 첫 번째 원소는 항상 물이기에 **k=0**일 때는 **pass**
  2. 이후 음식의 종류는 1, 2, 3, ... 순서대로 올라가기에 ```k+=1```을 하여 음식의 종류를 할당
  3. ```문자열 * 정수```를 하는 경우 문자열이 정수 크기 만큼 반복되므로 이를 이용해 왼쪽 사람이 먹는 음식 순서를 나열
  4. 음식 개수의 경우 2로 나눈 값의 몫을 이용해 각자 음식별로 먹어야하는 개수를 구함
  5. 가운데 물인 0을 넣어주고, ```[::-1]```를 이용해 오른쪽 사람이 먹는 음식 순서를 나열한 후 더해줌
  <br><br><br>
  
## 💡 느낀점
  1. 다른 스터디원들은 ```''.join.reversed()```를 이용하여 5번 과정을 해결하였는데, 또 하나의 방법을 알게되었다.
  2. 한 스터디원은 음식 개수를 나누어 줄 때 홀수와 짝수를 나누어 계산하였는데, 코드는 길어지지만 조금 더 확실하고 가독성이 좋았던 것 같다.

<br><br><br><br>

잘못된 내용이나 피드백은 언제나 환영입니다. <br>
출처 : 프로그래머스 코딩 테스트 연습, https://school.programmers.co.kr/learn/challenges
