# Person 클래스 구현하기

> #### 인스턴스 변수 생성
<pre><code>
class Person:
  def __init__(self,name,mobile = "010-1234-1234",office = "Office",email="abc123@gmail.com"):
    self.name = name
    self.mobile = mobile
    self.office = office
    self.email = email
</pre></code>

클래스 이름을Person르로 지정하고 name, mobile, office, email 인스턴스를 만든다.   
name은 입력받아야하고 mobile,office,email은 기본값을 지정해 두었다.

> ### __str__()매소드 정의
> 
<pre><code>
  def __str__(self):
    return f"name:{self.name}/ mobile:{self.mobile}/ office:{self.office}/email:{self.email}"
</pre></code>
name : 이름/ mobile: 전화번호/ office:주소/ email:이메일 로 출력되는 메소드 정의

> #### setName, getName 매소드 정의
<pre><code>
  def setName(self,name):
    self.name = name
  def getName(self):
    return self.name
</pre></code>
setName 매서드에서는 name를 받아서 수정할 수 있고   
getName 매서드는 저장된 name를 반환해서 확인할 수 있다.
> #### setMobile, getMobile 매소드 정의
<pre><code>
  def setMobile(self,mobile):
    self.name = mobile
  def getMobile(self):
    return self.mobile
</pre></code>

> #### setOffice,getOffice 매소드 정의
<pre><code>
  def setOffice(self,office):
    self.name = office
  def getOffice(self):
    return self.office
</pre></code>

> #### setEmail, getEmail 매소드 정의
<pre><code>
  def setEmail(self,email):
    self.name = email
  def getEmail(self):
    return self.email
</pre></code>

> ### 구현한 클래스와 매소드가 제대로 작동하는지 확인
<pre><code>
name = input("이름을 입력하세요: ")
person = Person(name)
print(person.getEmail())
person.setMobile("010-5678-5678")
print(person.__str__())
</pre></code>

이름을 입력받아 name에 저장하고 name을 인스턴스 변수로 사용하여 person이라는 클래스를 구현   
getEmail매서드를 통해 email값을 반환받아 출력한다.   
setMobile매서드를 통해 mobile값을  지정된 값으로 수정한다.   
\_\_str\_\_ 매소드를 통해 저장된 값들을문자열로 출력한다.
