# ClientMain

```java
package client;

import java.net.Socket;

public class ClientMain {
	public static void main(String[] args) {
		try { 
			
			Socket soc = new Socket("127.0.0.1", 55555); // 접속 시도
			
			ClientSendThread cst = new ClientSendThread();
			cst.setSocket(soc);
			
			ClientReceiveThread crt = new ClientReceiveThread();
			crt.setSocket(soc);
			
			cst.start();
			crt.start();
			
		} catch(Exception e) {
			e.printStackTrace();
		}
	}
}

```

