<h2>Content Beyond Syllabus<br>
Implementation of Remote Command Execution (RCE) 14-10-2021</h2>

<h6><b>AIM</b></h6>
To implement Remote Command Execution(RCE).

<h6><b>ALGORITHM</b></h6>
<b>CLIENT SIDE</b>


1. Establish a connection between the Client and Server.
Socket client=new Socket("127.0.0.1",6555);

2. Create instances for input and output streams.
Print Stream ps=new Print Stream(client.getOutputStream());

3. BufferedReaderbr=newBufferedReader(newInputStreamReader(System.in));

4. Enter the command in Client Window.
Send themessage to its output
str=br.readLine();
ps.println(str);

<b>SERVER SIDE</b>

1. Accept the connection request by the client.
ServerSocket server=new ServerSocket(6555);
Sockets=server.accept();

2. Getthe IPaddressfromitsinputstream.
BufferedReaderbr1=newBufferedReader(newInputStreamReader(s.getInputStream()));
ip=br1.readLine();

3. During runtime execute the process
311119205028 Krithika N
Runtime r=Runtime.getRuntime();
Process p=r.exec(str);

<h6><b>OUTPUT</b></h6>
A New notepad opened.
![Screenshot (992)](https://user-images.githubusercontent.com/76687631/142190304-3e2dd6a2-2d01-4508-a6ec-04f884394930.png)


<h6><b>RESULT</b></h6>
Thus the implementation RCE is done & executed successfully
