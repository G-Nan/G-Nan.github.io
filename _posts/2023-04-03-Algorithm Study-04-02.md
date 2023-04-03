---
layout: single
title: 4주차  번째 문제 - 분수의 덧셈
---





<br>
# Baekjoon의 [분수의 덧셈](https://school.programmers.co.kr/learn/courses/30/lessons/120808)라는 문제를 다 같이 풀어보았습니다.

<br><br><br>

## 📖 문제
![image](https://user-images.githubusercontent.com/97678547/229469597-d1ef8bb8-373e-4362-8a16-314c53423836.png)
<br><br><br>
 
## ✏️ 나의 풀이

  ```python
def divisor(num):
    elem = []
    for i in range(1, int(num**(1/2)) + 1):
        if num%i == 0:
            elem.append(i)
            elem.append(int(num/i))
            
    elem.sort()
    return elem
            
def max_divisor(num1, num2):
    gcd = 0
    
    divisor_num1 = divisor(num1)
    divisor_num2 = divisor(num2)
    print(divisor_num1, divisor_num2)
    for i in divisor_num1:
        if i in divisor_num2:
            gcd = i
            
    return gcd

def solution(numer1, denom1, numer2, denom2):
    
    denom = denom1 * denom2
    numer = numer1 * denom2 + numer2 * denom1
    
    max_div = max_divisor(denom, numer)
    
    denom = int(denom / max_div)
    numer = int(numer / max_div)
    
    return [int(numer), int(denom)]
  ```
  Point - 각각 약수를 구하여 최대 공약수를 구하고 덧셈 값을 최대 공약수로 나누어 줌
  1. 약수를 리스트에 담아주는 함수 **divisor**를 생성
  2. 각 약수 리스트에서 최대 공약수를 출력해주는 함수 **max_divisor**를 생성
  3. 분수 계산 법으로 **denom**, **numer** 변수에 할당
  4. **denom**, **numer**의 최대 공약수를 **max_div**에 할당
  5. 최대 공약수로 나누어주어 답을 출력



  <br><br><br>
  
## 💡 느낀점
  - **최대 공약수**만 구할 수 있다면 크게 어려움 없는 문제이다.
  - **약수**를 구하는 과정은 시간 복잡도가 $\sqrt{n}$인 방법을 활용하여 함수를 만들어주었다. 

<br><br><br><br>

잘못된 내용이나 피드백은 언제나 환영입니다. <br>
출처 : 백준, https://www.acmicpc.net/problemset
