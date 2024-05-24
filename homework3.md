# 나눗셈 계산기
> #### a, b 입력받기
<pre><code>
a, b = map(int, input("숫자 두개를 입력해주세요").split())
</pre></code>
map를 활용하여 한번에 입력받고 띄어쓰기를 기준으로 나누어 각각 a,b에 저장 
> ### 실행해볼 코드
<pre><code>
try :
  c= a / b
  print(f'{a} / {b} = {c}')
</pre></code>
try를 통해서 실행해볼 코드를 입력했다
입력받은 a를b로 나누고 출력해보는 코드

> ### 정수가 아니고 다른 것을 입력했을 때 처리할 코드
<pre><code>
except ValueError :
  print("입력한 숫자를 확인해주세요.")
</pre></code>
ValueError가 발생했을 때 처리할 코드

> ### 0으로 나누기를 시도했을 때 처리할 코드
<pre><code>
except ZeroDivisionError:
  print("0으로 나눌 수 없습니다.")
</pre></code>
b에 0을 입력했을 때 처리할 코드

> ### 오류가 없을 때 처리할 코드
<pre><code>
else :
  print(f'{a} / {b} = {c}')
</pre></code>
오류가 발생하지 않았을 때 a / b = c를 출력한다.

> #### 마무리
<pre><code>
finally :
  print("calculation completed")
마지막으로 계산이 완료되었음을 출력해준다.
</pre></code>
