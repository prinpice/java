# ClientTest

```java
package basic;

import java.io.BufferedReader;
import java.io.InputStream;
import java.io.InputStreamReader;
import java.io.OutputStream;
import java.io.OutputStreamWriter;
import java.io.PrintWriter;
import java.net.Socket;

import javax.swing.JOptionPane;

public class ClientTest {
	public static void main(String[] args) {
		try {
			// 1. 서버와 연결 + 서버와 통신하기 위한 소켓 생성
			Socket soc = new Socket("192.168.5.101", 55555); // 서버의 IP, 포트 번호
		//  127.0.0.1 ===> '나 자신'이라는 의미를 가진 IP (서버도 이 컴퓨터다)
			
			// (클라이언트의 소켓이 생성되면, Server 측의 accept()이 실행
			// (서버측에서도 소켓이 생성될 거임)
			
			// 2. 서버와 통신하기 위한 스트림 생성
			
			// 서버에게 데이터를 내보낼 스트림
			OutputStream out = soc.getOutputStream();
			
			// 서버에게 데이터를 받을 스트림 
			InputStream in = soc.getInputStream();
			
			// 속도 높이기 위해 보조스트림 설정
			PrintWriter pw = new PrintWriter(new OutputStreamWriter(out));
			BufferedReader br = new BufferedReader(new InputStreamReader(in));
			
			String inputData;
			while (true) { // 서버 접속이 끊길 동안
				inputData = JOptionPane.showInputDialog("서버에게 보낼 메세지(종료:exit)");
				if(inputData.equals("exit")) {
					break;
				}
				// 서버에게 데이터를 보냄
				pw.println(inputData);
				pw.flush();
				
				// 서버에게 데이터를 받음
				JOptionPane.showMessageDialog(null, "from Server: " + br.readLine());
			}
			pw.close();
			br.close();
			soc.close();
			
		} catch(Exception e) {
			e.printStackTrace();
		} 
		 
	}
}

```

