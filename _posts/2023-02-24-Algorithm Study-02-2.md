---
layout: single
title: 1주차 두 번째 문제 - 평행
---





# 1주차 두 번째 문제 
Programmers의 [평행](https://school.programmers.co.kr/learn/courses/30/lessons/120875)이라는 문제를 다 같이 풀어보았습니다.
<br><br><br>
> ## 📖 문제
> ![image](https://user-images.githubusercontent.com/97678547/221108110-234318aa-44ec-4a2a-967c-72d5851f50c9.png)
> <br><br><br>
> ## ✏️ 나의 풀이
>
>  ```python
>  def solution(dots):
>   answer = 0
>    
>   a1 = dots[0]
>   dots.remove(a1)
>    
>   for i in range(len(dots)):
>       a2 = dots[i]
>       b1 = dots[(i+1)%len(dots)]
>       b2 = dots[(i+2)%len(dots)]
>        
>       grad1 = (a1[1]-a2[1])/(a1[0]-a2[0])
>       grad2 = (b1[1]-b2[1])/(b1[0]-b2[0])
>       if grad1 == grad2:
>           answer = 1
>            
>   return answer
>  ```
>  1. 4개의 점을 2개 2개로 나누는 경우는 3가지이다. (0번-1번/2번-3번, 0번-2번/1번-3번, 0번-3번/1번-2번)
>  2. 그렇기에 한 점을 **a1**이라는 변수에 할당한 뒤 **dots**에서 제거해준다. (for문을 편하게 하기 위해) 
>  3. 0번과 이어지는 점이 각각 1번, 2번, 3번이므로 **for**문을 이용해 **a2**변수게 악각 할당한 후 나머지 두 점을 **b1**과 **b2**에 할당해준다. <br>
>  (이 때, **dots**는 현재 3개의 점이 있을 것이고, **a2**의 인덱스에 1과 2를 더해준 후 전체 길이로 나눈 나머지를 이용하여 각각 점을 할당해주었다.)
>  4. 이후 기울기 = y변화량 / x변화량 을 이용하여 각 직선의 기울기를 **grad1**과 **grad2**라는 변수에 할당해주었다.
>  5. 조건문을 사용하여 두 기울기가 같은 경우 1, 다른 경우 0이 나오게끔 하였다. <br>
>  (직선이 일치하는 경우도 출력값이 1이 나와야하므로 따로 일치하는 경우를 제거해주지는 않았다.)
>  <br><br><br>
> ## 💡 느낀점
>  1. 스터디원 중 한 명은 수학 식이 기억이 나지 않아 식을 사용하지 않고 푸는 방법을 제시하였다. <br>
>  깔끔하게 떨어지면 좋겠지만, 기억이 나지 않거나 잘 모르겠을 때에도 최선을 다하는 모습이 인상깊었다.

<br><br><br><br>
잘못된 내용이나 피드백은 언제나 환영입니다. <br>
출처 : 프로그래머스 코딩 테스트 연습, https://school.programmers.co.kr/learn/challenges
