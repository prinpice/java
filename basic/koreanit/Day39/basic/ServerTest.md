# ServerTest

```java
package basic;

import java.io.BufferedReader;
import java.io.InputStream;
import java.io.InputStreamReader;
import java.io.OutputStream;
import java.io.OutputStreamWriter;
import java.io.PrintWriter;
import java.net.InetAddress;
import java.net.ServerSocket;
import java.net.Socket;

public class ServerTest {
	public static void main(String[] args) {
		// 1. 서버 소켓 생성 + 55555번 포트로 바인딩
		ServerSocket sSoc = null;
		Socket soc = null;
		try {
			sSoc = new ServerSocket(55555);
			System.out.println("서버 소켓 생성...");
			System.out.println("클라이언트를 기다립니당...");
			
			soc = sSoc.accept(); 
			// 클라이언트가 오기를 기다림. 클라이언트가 오면 그 클라이언트와 연결할 소켓(soc)을 생성 
			
			System.out.println("클라이언트가 왔다!!!!");
			InetAddress clientAddress = soc.getInetAddress(); 
			System.out.println("(상대 IP : " + clientAddress + ")");
			System.out.println();
			
			// 클라이언트와 통신할 Stream을 생성
			OutputStream out = soc.getOutputStream(); // 클라이언트에게 데이터를 내보내기 위함
			InputStream in = soc.getInputStream(); // 클라이언트로부터 데이터를 받기 위함
			
			// 전송 속도를 높이기 위해서 스트림에 보조스트림 설정
			PrintWriter pw = new PrintWriter(new OutputStreamWriter(out));
			// out -> OutputStreamWriter로 변경 -> PrintWriter로 변경
			
			BufferedReader br = new BufferedReader(new InputStreamReader(in));
			// in -> InputStreamReader로 변경 -> BufferedReader로 변경
			// ** BufferedReader란? 
			//    대상에 미리 데이터를 받아서(버퍼링) 빠르게 읽을 수 있게 도와주는 보조스트림 
			
			String data = null;
			while( (data = br.readLine()) != null ) { 
				// data = br.readLine() 
				//  ====> 클라이언트로부터 들어온 데이터를 1줄(\n) 읽어옴 + data에 저장
				
				// data != null 
				//  ====> 클라이언트가 연결을 종료하면 스트림이 닫힘, 이때 readLine()하면 null이 리턴 
				
				System.out.println("from Client : " + data);
				pw.println(data); // 클라이언트에게 방금 그 data를 보냄
				pw.flush(); // 클라이언트 측에게 데이터를 모두 읽도록 함 + 버퍼를 깨끗하게 비움
			}
			
			// 스트림 닫기
			pw.close();
			br.close();
			soc.close();
		} catch(Exception e) {
			e.printStackTrace();
		} finally {
			try {
				if(sSoc != null) { // 서버 소켓이 살아있다면
					sSoc.close(); // 서버 소켓 없애기
				}
			} catch(Exception e) { e.printStackTrace(); }
		}
	}
}

```

