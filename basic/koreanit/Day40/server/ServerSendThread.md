# ServerSendThread

```java
package server;

import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.OutputStreamWriter;
import java.io.PrintWriter;
import java.net.Socket;

import javax.swing.JOptionPane;

public class ServerSendThread extends Thread{
	private Socket soc;
	
	public void setSocket(Socket soc) {
		this.soc = soc;
	}
	
	public void run() {
		try {
			// 사용자 입력용 스트림 (콘솔 입력용)
			BufferedReader br = new BufferedReader( new InputStreamReader(System.in) );
			
			// 클라이언트 발신용 스트림
			PrintWriter pw = new PrintWriter( new OutputStreamWriter( soc.getOutputStream() ) );
			
			String sendMessage; 
			System.out.println("(ServerSend 실행, 발신 종료는 exit)...");
			while(true) {
				sendMessage = br.readLine(); // 콘솔창에 입력 받은 문자열 1줄을 sendMessage에 저장
				if(sendMessage.equals("exit")) {
					break;
				}
				pw.println(sendMessage);
				pw.flush();
			}
			
		} catch (Exception e) {
			e.printStackTrace();
		}
	}
}












```

