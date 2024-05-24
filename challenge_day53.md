# 소인수를 오름차순으로 담은 배열를 반환하는 함수

> ####  소인수를 오름차순으로 반환하는 solution 함수 정의 
<pre><code>
def solution(n):   
  result = []   
  a = 2
</pre></code>
result를 빈 리스트로 만들어두고 a에 2를 저장한다.   

> ### 반복문 / n이 a로 나누어 질 때
<pre><code>
  while a <= n:
    if (n % a) == 0 :
      if a not in result:
        result.append(a)
      n /= a
</pre></code>
a가 n보다 작거나 같을 동안만 반복문을 돌림   
n을 a로 나눈 나머지가 0일때   
a가 result에 없는 값이라면 result리스트에 추가하고 있다면 중복이므로 리스트에 추가하지 않음   
그 후 n에 n를 a로 나눈 값을 저장함   

> ### 반복문 / n이 a로 나누어 지지 않을 떄
<pre><code> 
    else:
      a += 1
  return result
</pre></code>
나머지가 0이 아니라면(a로 나누어지지 않으면)   
a에 1을 더하면서 나누어지는 숫자를 찾는다.

> #### 만든 함수가 제대로 작동하는지 확인

<pre><code>
n = int(input("소인수분해할 숫자를 입력하세요: "))
print(solution(n))
</pre></code>
n 를 입력받아 int()를 이용해 정수로 바꾸어줌
위에서 정의한 solution함수에 매개변수로 n를 넣어   
입력한 숫자의 소인수가 무엇인지 출력함
