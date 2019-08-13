# ServerReceiveThread

```java
package server;

import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.net.Socket;import javax.sound.sampled.ReverbType;

// 서버 -> 클 에게 데이터 보낼 때 쓸 쓰레드
public class ServerReceiveThread extends Thread{
	private Socket soc;
	
	public void setSocket(Socket soc) {
		this.soc = soc;
	}
	
	public void run() {
		try {
			// 클라이언트에게서 수신한 데이터를 읽을 입력스트림 ( 소켓에 연결된 스트림)
			BufferedReader br = new BufferedReader( new InputStreamReader( soc.getInputStream()));
			
			String receivedMessage;
			
			while(true) {
				receivedMessage = br.readLine();
				if(receivedMessage == null) { // 클라이언트가 연결을 끊었을 경우
					System.out.println("클라이언트 연결 끊김..");
					break;
				}
				System.out.println("From Client : " + receivedMessage);
			}
			br.close();
			soc.close();
		} catch(Exception e) {
			e.printStackTrace();
		}
	}
}







```

