---
layout: single
title: 2주차 첫 번째 문제 - 주유소
---





# 2주차 첫 번째 문제
Baekjoon의 [주유소](https://www.acmicpc.net/problem/13305)라는 문제를 다 같이 풀어보았습니다.





<br><br><br>
 ## 📖 문제
![image](https://user-images.githubusercontent.com/97678547/222954411-b84da6c7-0f58-4f18-a142-67ae67987f24.png)
 <br><br><br>
 ## ✏️ 나의 풀이

  ```python
  x1 = int(input())
x2 = list(map(int, input().split( )))
x3 = list(map(int, input().split( )))
answer = 0

min_oil = x3[0]

for i in range(x1 - 1):
    if min_oil > x3[i]:
        min_oil = x3[i]
    answer += min_oil * x2[i]
    
print(answer)
  ```
  Point - 가장 낮은 기름 값으로 최대한의 거리를 가는 것  
  1. 우선 첫 번째 마을의 기름 가격을 **min_oil** 변수로 선언
  2. **for** 반복문을 이용하여 마을의 기름 값이 **min_oil**보다 낮아질 때 마다 **min_oil** 를 갱신
  3. **min_oil**값과 그 기름 값으로 가야하는 이동 거리를 곱하여 총 비용을 계산
  <br><br><br>
 ## 💡 느낀점
  - 처음 풀이를 하였을 때 실패를 하였는데, 그 이유는 전 마을과 다음 마을의 기름 가격을 비교하여 더 싼 기름 가격으로 가는 방법을 사용하였다. <br>
      하지만 이러한 방법을 사용하면 문제가 발생했는데 아래 예를 통해 보자면
      ```
        2   4   3 
      A - B - C - D  
      ```
      이러한 경우에서는 A부터 D까지 2의 가격으로 가는 것이 가장 저렴한 방법이다. <br>
      그러나 위의 방법대로 한다면 A에서 C까지는 2의 가격으로 가지만, C에서 D는 3의 가격으로 가기에 문제가 발생한다. <br>
      그렇기에 최소 기름 가격을 선언해준 후 갱신해준다는 아이디어로 전환하여 풀어주었다.
<br><br><br><br>
잘못된 내용이나 피드백은 언제나 환영입니다. <br>
출처 : 백준, https://www.acmicpc.net/problemset
