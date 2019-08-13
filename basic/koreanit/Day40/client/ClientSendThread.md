# ClientSendThread

```java
package client;
// 클라이언트 --> 서버에게 데이터를 보내는 스레드

import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.OutputStreamWriter;
import java.io.PrintWriter;
import java.net.Socket;

public class ClientSendThread extends Thread {
	private Socket soc; 
	public void setSocket(Socket soc) {
		this.soc = soc;
	}
	
	public void run() {
		try {
			
			// 사용자 입력용 스트림 (System.in)
			BufferedReader br = new BufferedReader( new InputStreamReader(System.in));
			
			// 서버에게 발신용 스트림 (소켓의 출력스트림)
			PrintWriter pw = new PrintWriter( new OutputStreamWriter(soc.getOutputStream()));
			
			System.out.println("(ClientSend 실행, 접속 종료는 exit)...");
			String sendMessage;
			while(true) {
				sendMessage = br.readLine(); // 한 줄 입력 받음
				if(sendMessage.equals("exit")) {
					break;
				}
				
				// 서버에게 전송 
				pw.println(sendMessage);
				pw.flush();
			}
			
			pw.close();
			br.close();
			soc.close(); // 소켓 종료 (통신 종료)
			
		} catch(Exception e) {
			e.printStackTrace();
		}
	}
}








```

