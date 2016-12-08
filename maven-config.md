when u use the maven in a proxied network, you have to set the $MAVEN_HOME/.m2/settings.xml. with proxy.
```
<settings>
  .
  .
  <proxies>
   <proxy>
      <id>example-proxy</id>
      <active>true</active>
      <protocol>http</protocol>
      <host>proxy.example.com</host>
      <port>8080</port>
      <username>proxyuser</username>
      <password>somepassword</password>
      <nonProxyHosts>www.google.com|*.example.com</nonProxyHosts>
    </proxy>
  </proxies>
  .
  .
</settings>
```
  attention: the http & https proxy has to be set separately.
when the http/https proxy required authentication you have to encrypt your password.

how to encrypt your password. https://maven.apache.org/guides/mini/guide-encryption.html#How_to_encrypt_server_passwords
