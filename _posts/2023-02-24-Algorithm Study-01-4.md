---
layout: single
title: 1주차 네 번째 문제 - 다음에 올 숫자
---






Programmers의 [다음에 올 숫자](https://school.programmers.co.kr/learn/courses/30/lessons/120924)라는 문제를 다 같이 풀어보았습니다.

<br><br><br>

 ## 📖 문제
 ![image](https://user-images.githubusercontent.com/97678547/221121950-fb6ac95f-e30c-43d9-80a1-f09ea64bf24c.png)
 <br><br><br>
 
 ## ✏️ 나의 풀이

  ```python
  def solution(common):
   answer = 0
   
   if common[0] + common[2] == 2 * common[1]:
       answer = common[0] + (common[1]-common[0]) * len(common)
   else:
       answer = common[0] * (common[1]/common[0]) ** len(common)
   return answer
  ```
  1. 고등학교 수학에서 배우는 수열을 활용
  2. 우선 등차수열인 경우와 등비수열인 경우로 나누었는데, 이 때 등차중항, 등비중항을 사용
  3. 등차수열인지 등비수열인지 판단한 이후 수열의 일반항을 활용
  <br><br><br>
  
 ## 💡 느낀점
  1. 단순히 등차중항, 등비중항과 일반항만을 이용한 쉬운 풀이지만, 이 공식이 기억이 나지 않는다면 어려울 것 같다. <br>
  (저는 수학을 전공해서 잊고 싶어도 잊을 수가 없습니다.)

<br><br><br><br>

잘못된 내용이나 피드백은 언제나 환영입니다. <br>
출처 : 프로그래머스 코딩 테스트 연습, https://school.programmers.co.kr/learn/challenges
