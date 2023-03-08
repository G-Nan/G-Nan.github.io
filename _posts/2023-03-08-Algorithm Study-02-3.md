---
layout: single
title: 2주차 세 번째 문제 - 셀프 넘버
---






# Baekjoon의 [셀프 넘버](https://www.acmicpc.net/problem/4673)라는 문제를 다 같이 풀어보았습니다.

<br><br><br>

## 📖 문제
![image](https://user-images.githubusercontent.com/97678547/223660274-01fbb61c-6640-46d8-88ad-5908bde283e6.png)
 <br><br><br>
 
## ✏️ 나의 풀이

  ```python
unit = []
a = 0

while a < 10000:
    value = 0
    b = []
    for i in range(len(str(a))):
        b.append(int(str(a)[i]))
    value += a + sum(b)
    unit.append(value)
    a += 1
unit = set(unit)

for i in range(1, 10001):
    if i not in unit:
        print(i)
  ```
  Point - 셀프 넘버가 아닌 수(여사건) 들을 먼저 찾은 후 이에 포함되지 않는 값들을 추출
  1. 셀프 넘버가 아닌 수가 되기 위해서는 생성자가 필요
  2. 생성자를 **a**로 두고, 생성자는 생성자로 인해 만들어지는 값보다 작은 값이므로, 생성자의 최대 크기를 10000으로 두고 반복문을 생성
  3. **a**로 인해서 생성되는 수 들을 모두 **unit**이라는 리스트에 넣어줌
  4. 이 후 1부터 10000까지의 수 중에서 **unit**에 포함되지 않는 숫자들을 출력
  <br><br><br>
  
## 💡 느낀점
  - 생성자로 인해서 생성되는 수를 나는 for문을 이용하여 만들어냈지만, 스터디원중 한 명은 아래와 같은 방법을 활용하였다.
  ```python
  i_list = i + sum(map(int, str(i)))
  ```
  - 여기서 i는 생성자이고, map 함수를 통해 각 자리수의 값들을 합해주는 코드를 만들었는데, 나의 코드보다 훨신 간단해진 것 같다.
  - 이외에도 자릿수마다 경우를 만들어 계산하는 등 여러가지 방법을 볼 수 있어서 좋았다.
<br><br><br><br>

잘못된 내용이나 피드백은 언제나 환영입니다. <br>
출처 : 백준, https://www.acmicpc.net/problemset
