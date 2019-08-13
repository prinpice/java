# ClientReceiveThread

```java
package client;

import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.net.Socket;

// 서버에게서 데이터를 수신할 스레드 
public class ClientReceiveThread extends Thread{
	private Socket soc;
	public void setSocket(Socket soc) {
		this.soc = soc;
	}
	
	public void run() {
		try {
			// 서버로부터 데이터를 수신할 입력 스트림
			BufferedReader br = new BufferedReader( new InputStreamReader( soc.getInputStream()));
			
			String receivedMessage;
			while(true) {
				receivedMessage = br.readLine(); 
				System.out.println("From Server : " + receivedMessage);
			}
		} catch(Exception e) {
			e.printStackTrace();
		}
	}
}





```

