# Python_01
Python
- IDLE (Python 3.13 64-bit)



## 실습 내용
Python 연습을 위해 IDLE 프로그램을 사용하여 다양한 리스트, 배열 표현 코딩 연습하기



작성 코드
<pre>
<code>
# 리스트
list_1 = [1, "가", 3.14, ["a", "신호등", "3"]]
print(list_1,  type(list_1))

#리스트로 1차원 배열 표현하기 : for 문 사용
list_2=[]
for i in range(1,7):
    list_2.append(i)
print(list_2, type(list_2))

#하나의 리스트로 2차원 배열 표현하기(1) : 직접입력
list_3=[[1,2,3], [4,5,6]]
print(list_3, type(list_3))

#하나의 리스트로 2차원 배열 표현하기 : for 문 사용(1)
list_4=[]
for i in range(2):
    list_1.append([0]*3)

print(list_4, type(list_4))

#하나의 리스트로 2차원 배열 표현하기 : for 문 사용(2)
list_5=[[0]*3 for i in range(2)]
print(list_5, type(list_5))

#배열 (1)
#방법 1 : 1차원 배열(numpy 사용하는 방법)
import numpy as np
arr=np.arange(1,7)
print(arr, type(arr))

#방법 2 : 1차원 배열(numpy 사용 방법)
import numpy as np
arr2=np.array([1,2,3,4,5,6])
print(arr2,type(arr2))

#방법 3 : 2차원 배열(numpy 사용 방법)
import numpy as np
arr3=np.array([[1,2],[3,4],[5,6]])
print(arr3)
</code>
</pre>



#### 실행 결과
![코드 실행 결과](./Python/images/python_01.png)
