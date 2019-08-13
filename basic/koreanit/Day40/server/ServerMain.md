# ServerMain

```java
package server;

import java.net.ServerSocket;
import java.net.Socket;
import java.util.Date;

public class ServerMain {
	public static void main(String[] args) {
		try {
			ServerSocket sSoc = new ServerSocket(55555);
			
			System.out.println("클라이언트 연결을 기다립니다...");
			Socket soc = sSoc.accept();
			System.out.println("클라이언트와 연결 성공! " + new Date());
			
			// 쓰레드 실행 
			ServerSendThread sst = new ServerSendThread();
			sst.setSocket(soc); // 현재 소켓 정보를 스레드에게 넘겨줌
			sst.start(); // 스레드 실행
			
			ServerReceiveThread srt = new ServerReceiveThread();
			srt.setSocket(soc);
			srt.start();
			
		} catch(Exception e) {
			e.printStackTrace();
		}
	}
}







```

