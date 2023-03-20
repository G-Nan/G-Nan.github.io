---
layout: single
title: 3주차 두 번째 문제 - 행렬 덧셈
---






# Baekjoon의 [행렬 덧셈](https://www.acmicpc.net/problem/2738)라는 문제를 다 같이 풀어보았습니다.

<br><br><br>

## 📖 문제
![image](https://user-images.githubusercontent.com/97678547/226269890-9acb896a-b6ad-4faa-8686-7502e467acad.png)
<br><br><br>
 
## ✏️ 나의 풀이

  ```python
size = list(map(int, input().split()))
mat = []
for i in range(2 * size[0]):
    element = list(map(int, input().split()))
    mat.append(element)
    
mat1 = mat[:size[0]]
mat2 = mat[size[0]:]

for i in range(size[0]):
    for x, y in zip(mat1[i], mat2[i]):
        print(x + y, end = ' ')
    print('')
  ```
  Point - 각 행렬을 받아온 후 **이중 for문**과 **zip**을 이용하여 합하여 출력
  1. 두 행렬을 **mat1, mat2**에 할당
  2. **for**문의 **zip**을 활용하여 각 행렬 원소의 합을 구하여 출력
  > **zip 설명** <br>
  > 두 리스트의 원소를 각각 불러내는 방법
  >```
  >a = [1, 2, 3, 4]
  >b = [5, 6, 7, 8]
  >
  >for i, j in zip(a, b):
  >    print(i, j)
  >```
  > 출력
  > ``` python
  > 1, 5
  > 2, 6
  > 3, 7
  > 4, 8
  > ```
  > 
  <br><br><br>
  
## 💡 느낀점
  - 이중 for문과 zip을 활용하는 기본적인 문제였다.
  - 입력값을 받아오는 방법과 반복문에 따라 다양한 방법이 존재했다.

<br><br><br><br>

잘못된 내용이나 피드백은 언제나 환영입니다. <br>
출처 : 백준, https://www.acmicpc.net/problemset
