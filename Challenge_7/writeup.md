Challenge Description : Retrieve the hidden flag by analyzing the network traffic from the given packet capture file. 

Analysis : It is said that the attacker logged into the system without authorization. When he entered the credentials and logged in, the server sends an HTTP 200 OK status message which indicates a successful login. I filtered the network traffic for HTTP/1.1 200 OK status packets. The packet payload contained the flag. This was possible because the server used HTTP protocol and thus the content was plaintext. Flag had been hardcoded in the welcome.html http response. 

Final Flag : flag{analyzing_is_imp}
