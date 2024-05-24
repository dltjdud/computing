from itertools import combinations

def is_prime(n):
    for i in range(2,n):
        if (n % i) == 0:
            return False
            break
    if n == 2 :
        return False
    return True


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

nums = list(map(int,input().split()))
print(f"{nums}: {solution(nums)}개")
