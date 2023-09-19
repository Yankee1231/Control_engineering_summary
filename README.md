# **2주차 강의요약**    
2019732078 이성민    

***
> ## **글씨 크기 변경**
***
* '#'의 개수가 많을수록 글씨 크기가 작아진다.
###### 굵게6
##### 굵게5
#### 굵게4
### 굵게3
## 굵게2
# 굵게1
***


> ## **코드 블럭**
***
* grave라고 하는 기호 세 개(''')로 코드를 감싸면 코드 블럭을 만들 수 있습니다. 또한 grave 뒤에 언어를 적으면 특정 언어에 맞는 syntax highligh 기능을 사용할 수 있습니다.   
  * python
```python
import something
a = 10
print(a)
if a>10:
  print(a)
  ```
  * C
```c
#include <stido.h>
int main()
{
a = 10;
printf(%d, "a");
if a>10
  printf(%d, "a");
}  
```
***



> ## **수식 표현**
***

1. ### 수식의 정렬
* 왼쪽정렬(기본)  
 `$`로 수식의 앞 뒤를 감싸면 수식을 작성할 수 있습니다.   
$\begin{matrix}1&2\\3&4\\ \end{matrix}$
$\begin{pmatrix}1&2\\3&4\\ \end{pmatrix}$
$\begin{bmatrix}1&2\\3&4\\ \end{bmatrix}$
$\begin{Bmatrix}1&2\\3&4\\ \end{Bmatrix}$
$\begin{vmatrix}1&2\\3&4\\ \end{vmatrix}$
$\begin{Vmatrix}1&2\\3&4\\ \end{Vmatrix}$   
문장내 $\frac{1+s}{s(s+2)}$ 삽입
* 중앙정렬
$$\frac{1+s}{s(s+2)}$$  
* 특정 문자를 기준으로 정렬  
일반적으로 수식을 전개할 때 `=`기호를 기준으로 정렬합니다.
하지만 그냥 중앙정렬을 하면 다음과 같이 보입니다.
$$
f(x) = ax^2+bx+c\\
g(x) = Ax^4
$$
이때 `alingned` 심볼을 통하여 특정 문자를 기준으로 정렬할 수 있습니다. 정렬 기준은 `
$$
\begin{aligned}
f(x)&=ax^2+bx+c\\
g(x)&=Ax^4
\end{aligned}$$  
***


2. ### 수식내에서의 줄바꿈
* 수식에서 `Enter key`를 누른다고 해서 줄바꿈이 되지 않습니다. `\\`를 입력하면 줄바꿈을 할 수 있습니다.   
`$$x+y=3\\-x+3y=2$$`
$$x+y=3\\-x+3y=2$$
* 수식 안에서는 띄어쓰기를 해도 적용되지 않습니다. 다음과 같이 명시적으로 띄어쓰기를 입력하여야 합니다.  
`$local minimum$(띄어쓰기 적용 X)`    
`$local\,minimum$(띄어쓰기 한 번)`    
`$local\;minimum$(띄어쓰기 두 번)`    
`$local\quad minimum$(띄어쓰기 네 번)`      
$local minimum$(띄어쓰기 적용 X)  
$local\,minimum$(띄어쓰기 한 번)  
$local\;minimum$(띄어쓰기 두 번)  
$local\quad minimum$(띄어쓰기 네 번)  
***


3. ### 곱셈 기호
* 의외로 많이 쓰나 잘 알지 못하는 기호인 것 같습니다.
`y = A \times x + B`  
y = A \times x + B
***


4. ### 첨자
* 위 첨자는 `^` 기호로, 아랫 첨자는 `_` 기호로 적습니다.  
오른쪽에 한 글자가 자동으로 첨자로 들어가게 되고 두 글자 이상을 적용하려면 `{}`(중괄호)로 감싸면 됩니다.  
`$a_1, a^2, a_1^2$`  
`$y_i=x_i^3+x_{i-1}^2+x_{i-2}$`  
$$a_1, a^2, a_1^2$$
$$y_i=x_i^3+x_{i-1}^2+x_{i-2}$$
***


5. ### 분수 표기법
* 분수 표기법에는 두 가지 방법이 있습니다.
  * `\over`를 사용하면 \over를 기준으로 왼쪽에 있는 수식은 모두 분자, 오른쪽에 있는 수식으 모두 분모로 들어가게 됩니다.
  * `\frac`을 사용하게 되면 첫 번째 문자는 분자, 두 번째 문자는 분모로 들어가게 됩니다. 두 문자 이상이라면 중괄호 `{}`를 통하여 묶어주면 됩니다.  
`$s^2+2s+s\over s+\sqrt s+1$`  
`$\frac{1+s}{s(s+2)}$`  
$s^2+2s+s\over s+\sqrt s+1$  
$\frac{1+s}{s(s+2)}$  
***


6. ### 절대값 표기법
* 일반저긍로 절대값을 표기할 때는 키보드 위의 `|` 문자를 사용하게 됩니다.  
하지만 이렇게 하면 분수와 같이 큰 객체에 맞게 resizable한 기호를 사용할 수 없습니다.  
그럴 땐 `\vert`와`\left`,`\right`를 통하여 좌우 기호를 명시해주면 됩니다.  
`$\vert x \vert$`  
`$\left\lvert \frac{s^2+1}{s^3+2s^2+3s+1} \right\rvert$`  
$\vert x \vert$  
$\left\lvert \frac{s^2+1}{s^3+2s^2+3s+1} \right\rvert$  
***


7. ### sin, log와 같은 기호를 세워서 표기
* 단어 앞에 `\`를 붙이게 되면 똑바로 글자를 쓸 수 있습니다.  
Markdown에서 명시 되어 있지 않은 수학 단어라면 오류가 발생합니다.  
$\log_{10}{(x+1)}$
$A\sin(bx+c)$

****
> ## **표 (Table)**
***

* ### 표의 생성
  * `|`기호로 열을 구분하고 줄바꿈으로 행을 구분합니다.  
`|-|-|-|`가 헤더와 데이터를 구분하는 역할을 합니다.  
(없으면 표가 생성되지 않습니다. 안에 들어가는 `-`의 개수는 표시되는 표와 무관합니다.)  
`| 1열 | 2열 | 3열 |`  
`| :-------- | -----: | :------: |`  
`| 바디1 | 바디2 | 바디3 |`  
`| 바디4 | 바디5 | 바디6 |`  
  

| 1열 | 2열 | 3열 |  
| :-------- | -----: | :------: |  
| 바디1 | 바디2 | 바디3 |  
| 바디4 | 바디5 | 바디6 |  

***
> ## **기호**
***
* ### 화살표
  * 왼쪽 화살표와 오른쪽 화살표는 다음과 같이 적습니다.  
`$\larr$`  
`$\rarr$ or $\to$`    
$\larr$ (이거 잘 모르겠)  
$\to$

***
> ## **사진**
***
* 사진은 `!` 표시 뒤에 넣고 이미지에 대한 링크를 넣으므로써 해당 사진을 표출할 수 있다.
`![이미지](https://search.pstatic.net/common/?src=http%3A%2F%2Fblogfiles.naver.net%2FMjAyMzAzMzFfMTE3%2FMDAxNjgwMTkxNDUyOTYy.bFl0vxSSme7vK6-_yGmMDGesGqeY93RZxaZXsRBKr2Eg.-DQTTh5W_UWFSM1UuEF9dwejB7AUySmnsWYM3LZ1g98g.PNG.lytoo3%2F20230331_004852.png&type=l340_165)`

![이미지](https://search.pstatic.net/common/?src=http%3A%2F%2Fblogfiles.naver.net%2FMjAyMzAzMzFfMTE3%2FMDAxNjgwMTkxNDUyOTYy.bFl0vxSSme7vK6-_yGmMDGesGqeY93RZxaZXsRBKr2Eg.-DQTTh5W_UWFSM1UuEF9dwejB7AUySmnsWYM3LZ1g98g.PNG.lytoo3%2F20230331_004852.png&type=l340_165)

***
> ## **체크박스**
***
* [ ] 비어있는 체크박스  
* [x] 체크된 체크박스
