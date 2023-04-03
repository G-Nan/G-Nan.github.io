---
layout: single
title: 4주차  세 번째 문제 - 색종이
---





<br>

# Baekjoon의 [색종이](https://www.acmicpc.net/problem/2563)라는 문제를 다 같이 풀어보았습니다.

<br><br><br>

## 📖 문제
![image](https://user-images.githubusercontent.com/97678547/229473895-6cf40be4-8c8d-4a25-914b-cd2890c3e4d3.png)
<br><br><br>
 
## ✏️ 나의 풀이

  ```python
x0 = int(input())
x = [list(map(int, input().split())) for _ in range(x0)]

coord = []
for c in x:
    for i in range(10):
        for j in range(10):
            coord.append([c[0] + i, c[1] + j])
            
print(len(set(list(map(tuple, coord)))))
  ```
  Point - **반복문**을 이용해 각 색종이가 덮이는 부분을 모두 리스트에 넣어준 후 리스트 원소 개수를 이용해 계산
  1. **이중 for문**을 이용해 각 색종이가 덮이는 부분을 **coord** 리스트에 넣어줌
  2. 중복을 제거해주기 위해 **set**으로 바꾼 후 **len**을 이용해 원소 개수를 출력 


  <br><br><br>
  
## 💡 느낀점
  - **반복문**을 사용하지 않고 풀어보려고 시도했지만, 방법이 쉽게 떠오르지 않았다.

<br><br><br><br>

잘못된 내용이나 피드백은 언제나 환영입니다. <br>
출처 : 백준, https://www.acmicpc.net/problemset
