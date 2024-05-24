# circular prime 찾기
<pre><code>
import itertools
</code></pre> 
itertools 모듈을 불러옴 

> #### 매개변수가 소수인지 확인
<pre><code>
def is_prime(n) :
  for i in range(2,int(n)):
    if (int(n) % i) == 0:
      return False
      break
  if n == "2":
    return False
  return True
</code></pre> 
n를 받아서 2부터 n-1까지 i로 반복문을 돌려서   
n를i로 나눈 나머지가 0인 경우가 나오면 False를 반환하고 반복문을 탈출한다.   
0인 경우가 나오지 않는다면 반복문을 나온 뒤에 True를 반환한다.

> ### 재배열가능 소수인지 확인하는 함수
<pre><code>

def circular_prime(n):
  arr = [] 
배열를 바꿀 숫자들을 저장할 빈 리스트를 만듦   

> #### 숫자 배열 바꾸기
<pre><code>
  for i in str(n):
    arr.append(i)
    nPr = itertools.permutations(arr,len(str(n)))
  numbers = list(nPr)
</code></pre> 
빈 리스트에 입력받은 정수를 한 자리씩 나누어 저장하고   
permutations를 이용하여 numbers에 여러가지 경우를 저장

> #### 바꾼 배열이 모두 소수인지 확인
<pre><code>
  for item in numbers:
    number = ''.join(item)
    if is_prime(number) == False:
      return False
      break
  return True
</code></pre> 
반복문으로 numbers안의 각각의 경우를 확인함
join 메서드를 사용하여 각각의 경우를 number에 정수로 만들어줌   
위에서 정의한 is_prime함수를 사용하여 number가 소수인지 확인   
반복문을 돌면서 number 중 소수가 아닌 것이 있다면 False를 반환하고 반복문 종료   
없다면 반복문이 종류되고 True반환   
 
> #### 2부터 1000000사이에서 재배열 가능 소수를 리스트로 만들어서 출력
<pre><code>
result = []
for n in range(2,1000001):
  if circular_prime(n) == True:
    result.append(n)
print(result)
</code></pre> 
2부터 1000000까지의 수로 반복문을 돌려서   
circulat함수를 이용하여 재배열 가능 소수에 해당하는 값만 result리스트에 더함   
result 리스트를 출력함
</code></pre>
