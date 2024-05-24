# 더해서 몇개의 소수를 만들 수 있나

<pre>
<code>
from itertools import combinations
</code>
</pre>
> 소수 판별하는 함수
<pre>
<code>
def is_prime(n):
    for i in range(2,n):
        if (n % i) == 0:
            return False
            break
    if n == 2 :
        return False
    return True
</code>
</pre>
n를 매개변수로 하여서 2부터 n-1까지의 숫자로 n를 나누어서   
나머지가 없다면 False를 리턴하고 반복문을 벗어나고    
계속 나머지가 존재하고 반복문이 종료된다면 True를 리턴함

> 더해서 몇개의 소수를 만들 수 있는지 확인하는 함수
<pre>
<code>
def solution(nums):
    count = 0
    combs = list(combinations(nums,3))
    for c in combs:
      n = 0
      for i in c:
        n += i 
      print(n)
      if is_prime(n) == True:
        count += 1
    return count
</code>
</pre>
소수의 개수(count)를 0개로 설정해두고 combinations를 이용하여 조합을 만듦   
for문을 이용하여 리스트 안의 3가지 숫자를 선택하고 중첩된for문을 사용하여 3개의 숫자를 더해서 n에 저장   
그 후에 위에서 정의한 is_prime함수를 이용해서 n이 소수인지를 판별하고 소수라면 count에 1을 더함   
반복문을 종료한 뒤에 count값을 리턴함

> 제대로 작동하는지 확인(입력은 띄어쓰기로 구분함)
<pre>
<code>
nums = list(map(int,input().split()))
print(f"{nums}: {solution(nums)}개")
</code>
</pre>
map을 이용해 한번에 여러개의 숫자를 입력받고 각각의 숫자를 띄어쓰기를 기준으로 구분하여 리스트로 만듦   
입력받은 숫자 리스트와 각 숫자 중 3개의 조합으로 만들 수 있는 소수의 개수를 print함
