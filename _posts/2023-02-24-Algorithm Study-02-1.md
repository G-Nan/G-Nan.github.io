---
layout: single
title: 1주차 첫 번째 문제 - 둘만의 암호
---





# 1주차 첫 번째 문제
Programmers의 [둘만의 암호](https://school.programmers.co.kr/learn/courses/30/lessons/155652)라는 문제를 다 같이 풀어보았습니다.





<br><br><br>
> ## 📖 문제
> ![image](https://user-images.githubusercontent.com/97678547/221104558-7565a0ba-6540-4169-b4b2-b4963718eed4.png)
> <br><br><br>
> ## ✏️ 나의 풀이
>
>  ```python
>  def solution(s, skip, index):
>      apb = 'abcdefghijklmnopqrstuvwxyz'
>      
>      for i in skip:
>          apb = apb.replace(i, '')
>      
>      answer = ''
>    
>      for i in s:
>          answer += apb[(apb.index(i) + index)%len(apb)] 
>        
>      return answer
>  ```
>  1. 알파벳 문자열을 생성
>  2. **skip**에 포함된 문자열을 알파벳 문자열에서 제거
>  3. 이후 **s**문자열을 **index**만큼 오른쪽으로 옮겨준 값을 구함
>  4. 알파벳 문자열을 넘어가는 경우 다시 돌아오도록 나눗셈의 몫을 활용
>  <br><br><br>
> ## 💡 느낀점
>  1. 스터디원 중 한 명은 먼저 index만큼 옮겨준 뒤 skip의 문자열을 제거하려다 실패했다고 한다. <br>
>     (이렇게 하는 경우 조건문을 사용하기에 조금 더 복잡해 질 수 있으므로 잘 안되는 경우에 순서를 바꿔보는 것도 좋은 방법이다.)

<br><br><br><br>
잘못된 내용이나 피드백은 언제나 환영입니다. <br>
출처 : 프로그래머스 코딩 테스트 연습, https://school.programmers.co.kr/learn/challenges
