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
> 제대로 작동하는지 확인(입력은 띄어쓰기로 구분함)
<pre>
<code>
nums = list(map(int,input().split()))
print(f"{nums}: {solution(nums)}개")
</code>
</pre>
