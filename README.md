### Testing

Do these things

`docker run -it williamyeh/java7 bash`
Get the source in there or the class.  Compile/run whatever you gotta dew.

It'll break.  That's what you want...I guess...For testing tho!

```
root@57066bffe9f0:/javaGetTest/src# java -cp . testGet
 Send Https GET
Exception in thread "main" javax.net.ssl.SSLException: Received fatal alert: protocol_version
	at sun.security.ssl.Alerts.getSSLException(Alerts.java:208)
	at sun.security.ssl.Alerts.getSSLException(Alerts.java:154)
	at sun.security.ssl.SSLSocketImpl.recvAlert(SSLSocketImpl.java:1979)
	at sun.security.ssl.SSLSocketImpl.readRecord(SSLSocketImpl.java:1086)
	at sun.security.ssl.SSLSocketImpl.performInitialHandshake(SSLSocketImpl.java:1332)
	at sun.security.ssl.SSLSocketImpl.startHandshake(SSLSocketImpl.java:1359)
	at sun.security.ssl.SSLSocketImpl.startHandshake(SSLSocketImpl.java:1343)
	at sun.net.www.protocol.https.HttpsClient.afterConnect(HttpsClient.java:559)
	at sun.net.www.protocol.https.AbstractDelegateHttpsURLConnection.connect(AbstractDelegateHttpsURLConnection.java:185)
	at sun.net.www.protocol.http.HttpURLConnection.getInputStream(HttpURLConnection.java:1301)
	at java.net.HttpURLConnection.getResponseCode(HttpURLConnection.java:468)
	at sun.net.www.protocol.https.HttpsURLConnectionImpl.getResponseCode(HttpsURLConnectionImpl.java:338)
	at testGet.sendGet(testGet.java:30)
	at testGet.main(testGet.java:13)
root@57066bffe9f0:/javaGetTest/src#
```