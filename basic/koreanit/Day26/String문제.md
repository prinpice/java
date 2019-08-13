# String문제

```java
회원 가입 구현하기 
- ID, Password, Email

1. Email 입력받기   
 - @가 있어야함    ===> contains()
 - .com, .co.kr, .net 중 1개로 끝나야 함 ===> endsWith()
 - 단, 다음은 안됨 
    issell@.com  (도메인이 정확해야 함) ===> contains()
    @naver.com  ===> startsWith()

2. Password 입력 받기 
 - 4자 이상 ~ 12자 이하여야 함 ===> length()
 - 비밀번호를 한 번 더 입력 받고 두 비밀번호가 일치해야 함 ===> equals()

3. ID 설정하기 
 - 등록된 이메일의 아이디만 추출하여 ID로 자동 설정 ===> indexOf(), substring()

=> 위 규칙에 어긋났을 경우 그 부분을 다시 입력 받음 
=> 모든 설정이 끝나고 정보 출력 (비밀번호는 앞 두 글자만 보여주고 나머지는 '*' 처리) ===> length(), substring(), for문
 예)
 	[회원 가입에 감사드립니다.]
	ID : issell
	EMAIL : issell@naver.com
	PASSWORD : tp*******

```

