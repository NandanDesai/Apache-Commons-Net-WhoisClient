# Apache-Commons-Net-WhoisClient
WhoisClient extracted from the Apache Commons Net 3.6 API.

I wanted to use just the *whois* package from [Apache Commons Net library](https://commons.apache.org/proper/commons-net/). So, I extracted the code and made it into a separate repo so that some day it might be helpful for others who want a separate [Whois](https://en.wikipedia.org/wiki/WHOIS) Java library.

For JavaDoc, click [here](https://commons.apache.org/proper/commons-net/apidocs/org/apache/commons/net/whois/WhoisClient.html).

Example:
```java
WhoisClient whois;
whois = new WhoisClient();
try {
  whois.connect(WhoisClient.DEFAULT_HOST);
  System.out.println(whois.query("google.com"));
  whois.disconnect();
} catch(IOException e) {
  System.err.println("Error I/O exception: " + e.getMessage());
  return;
}
```
Include *WhoisClient.jar* file in your project and start using!
