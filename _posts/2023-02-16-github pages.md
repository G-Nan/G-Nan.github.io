---
layout: single
title: "Github Pages [1] 글 쓰는 법"
author: G-Nan
date: '2023-02-16 13:34:00'
---

# 글 정보 입력 

```
---
layout: 
title: 
author: 
date: 
category: 
thumbnail:
---
```

# 자주 사용되는 마크다운 문법
## 1. 헤더(Header)

💡 ```<h1>```부터 ```<h6>```까지 있으며, 점점 크기가 작아집니다. <br>
💡 ```#```은 6개 까지만 사용 가능합니다.

```
# This is h1
## This is h2
### This is h3
#### This is h4
##### This is h5
###### This is h6
```

💡 ```<h1>```과 ```<h2>```는 다음과 같이 표현할 수 있습니다.

``` 
This is h1
==========

This is h2
----------
```

# This is h1
## This is h2
### This is h3
#### This is h4
##### This is h5
###### This is h6

<br><br><br><br>
------------------
# 2. 줄바꿈
💡 ```<br>```을 이용하여 줄을 바꿀 수 있습니다.

```
This is first sentence. <br>
This is second sentence.
```

This is first sentence. <br>
This is second sentence.

💡 문장 마지막에 3칸 이상 띄어쓰기를 하면 줄을 바꿀 수 있습니다.

```
This is first sentence. _________   <- 띄어쓰기    
This is second sentence.
```

This is first sentence.    
This is second sentence.

<br><br><br><br>
------------------
# 3. 인용
💡 ```>```를 이용하여 인용문을 만들 수 있습니다. <br>
💡 ```>```는 3개까지만 사용 가능합니다.
```
> This is first blockqute.
>> This is second blockqute.
>>> This is third blockqute.
```
> This is first blockqute.
>> This is second blockqute.
>>> This is third blockqute.

💡 인용문 안에 다른 마크다운 요소를 포함할 수 있습니다

```
> This is first blockqute.
- List
'''
Code
'''
```

> This is first blockqute.
- List
```
Code
```

<br><br><br><br>
------------------
# 4. 강조
- 특정 문자로 텍스트를 감싸주는 형태

### 기울이기 <br>

💡 ```*``` 또는 ```_```으로 문장을 감싸줍니다.
```
*This is italic.*
_This is italic._
```
*This is italic.* <br>
_This is italic._

### 굵게쓰기 <br>

💡 ```**``` 또는 ```__```으로 문장을 감싸줍니다.
```
**This is bold.**
__This is bold.__
```
**This is bold.** <br>
__This is bold.__

### 취소선 <br>

💡 ```~~```으로 문장을 감싸줍니다.
```
~~This is canceled.~~
```
~~This is canceled.~~

<br><br><br><br>
------------------

# 5. 목록
- 목록은 <u>순서가 없는 목록</u>과 <u>순서가 있는 목록</u>으로 나뉩니다.

### 순서가 없는 목록
💡 ```*```, ```+```, ```-```를 이용하여 만들 수 있습니다. <br>
💡 들여쓰기를 이용하여 모양을 바꿀 수 있습니다. <br>
💡 서로 섞어서 사용해도 문제가 없습니다. <br>

```
* first
    * second
        * third
    
+ first
    * second
        - third
```

* first
    * second
        * third
    
+ first
    * second
        - third
<br><br>

### 순서가 있는 목록
💡 숫자를 사용하여 만들 수 있습니다. <br>
💡 숫자와 상관없이 순서대로 숫자가 정해집니다. <br>

``` 
1. first
2. second
7. third
5. fourth
```
1. first
2. second
7. third
5. fourth

<br><br><br>
계속 내용을 추가해나갈 예정입니다. <br>
잘못된 내용이 있으면 피드백 부탁드립니다.