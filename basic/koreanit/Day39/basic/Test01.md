# Test01

```java
package basic;

import java.net.InetAddress;

/*
 * < 네트워크 프로그래밍 > 
 *  - IP : 컴퓨터가 가지는 고유 주소
 *     공인 IP : 홈네트워크가 외부 네트워크와 통신할 때 사용하는 IP
 *     			(우리 학원의 공인 아이피는 1개)
 *     사설 IP : 하나의 홈네트워크(기업끼리의, 집안에서의) 소속의 
 *              컴퓨터 IP
 *              (우리 학원의 각 컴퓨터들은 모두 같은 공인 IP를 가지고 있지만 
 *               사설 IP 주소가 모두 다름)
 *  - 포트(port) : 하나의 컴퓨터가 여러 서비스를 제공하기 위해 사용하는 정보
 *    --> 컴퓨터 : 빌딩 
 *        포트 : 빌딩 안의 사무실 번호
 *    --> 통신을 하기 위해서는 " 주소 + 서버의 포트번호 " 가 필요함
 *        
 *  - 바인딩  : 연결
 *    --> 서버의 서비스와 포트번호를 연동 
 *  
 *  - 통신의 원리 : Server-Client
 *    Server : request에 대한 response를 하는 대상
 *    Client : 서버에게 request를 하는 대상
 *    
 *  - TCP vs UDP 통신
 *    1) TCP : 연결지향 통신 프로토콜
 *     : 데이터를 보낸 뒤, 상대에게 '잘 받았다'라는 메세지를 받아야 
 *       다음 데이터를 보냄 
 *      - 장점 : 신뢰성이 높다.
 *      - 단점 : UDP보다 느리다.
 *      - 종류 : HTTP, HTTPS (우리가 사용하는 인터넷)
 *      
 *    2) UDP : 비연결지향 통신 프로토콜
 *      : 연결 여부를 확인하지 않고, 데이터를 쭉 보냄
 *      - 장점 : 빠르다 
 *      - 단점 : 신뢰도가 낮다
 *      - 종류 : 전화, 무전기, 라디오 
 */



public class Test01 {
	public static void main(String[] args) {
		try {
			InetAddress address = InetAddress.getLocalHost();
			System.out.println(address);
			
			InetAddress[] naveraddress = InetAddress.getAllByName("www.naver.com");
			
			System.out.println("네이버 서버들의 IP 주소");
			for(InetAddress ip : naveraddress) {
				System.out.println(ip);
			}
		} catch(Exception e) {
			e.printStackTrace();
		}
	}
}





```

