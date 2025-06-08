# Python_02
Python
- IDLE (Python 3.13 64-bit)



## 실습 내용
Python 연습을 위해 IDLE 프로그램을 사용하여 최대공약수(GCD)를 구하는 함수(유클리드 호제법을 사용)



작성 코드
<pre>
<code>
def gcd(a, b):
    if b == 0:
        # b가 0이 되면 a가 최대공약수
        return a
    else:
        # b가 0이 아니라면, a를 b로 나눈 나머지를 이용해 재귀적으로 호출
        return gcd(b, a % b)

# 최소공배수(LCM)를 구하는 함수
def lcm(a, b):
    n = gcd(a, b)          # 먼저 두 수의 최대공약수를 구함
    return (a * b) // n    # 최소공배수 공식: (a * b) / gcd(a, b)
                           # 정수 나눗셈을 사용하여 정확도와 성능을 확보

# 테스트 케이스 실행
# 각각의 함수가 올바르게 작동하는지 확인하기 위해 다양한 입력을 사용

print(gcd(10, 12))   # 출력: 2 (10과 12의 최대공약수)
print(gcd(12, 18))   # 출력: 6 (12와 18의 최대공약수)

print(lcm(3, 4))     # 출력: 12 (3과 4의 최소공배수)
print(lcm(12, 18))   # 출력: 36 (12와 18의 최소공배수)
</code>
</pre>



#### 실행 결과
![코드 실행 결과](/Python/images/python_02.png)
