<img src="/PBQ/pbq1.jpeg" alt="performance-based-questions" width="800px">
<img src="/PBQ/pbq2.jpeg" alt="performance-based-questions" width="800px">

<hr>

<p>
    This is a practice question derived from <a href="https://www.youtube.com/watch?v=IdtwOqsF5KY"> Cyberkraft </a> about firewall rules. 
</p>
<p> 
    On the exam, make sure to not follow each step according to each rule. They may be scattered where question 1 might refer to firewall rule number 6. 
</p>
<p> 
    🛡️In the first question, we want to set the source IP address for rule 1 to "any". This is because in the question it tells us to allow HTTP and HTTPS traffic from any external IP address to head to the web server. In this case, we are dealing with port 80 which is HTTP. We will set the action to "allow" in order for the traffic to reach the web server. Also, in rule 2 since we are dealing with HTTPS based on port 443, we need to set the destination IP address to (10.0.0.1) because that is the IP address of the web server. 
</p>
<p> 
    🛡️In the second question, we simply need to allow SSH traffic from the internal network to the database server where the question asks us the specific port number. Since we need to allow SSH traffic, we will set it to port 22 because SSH operates on that port number.  
</p>
<p>
    🛡️For the third question, we need to allow DNS queries from any device on the internal network to head to the DNS server. Based on question 2 and the firwall rules, we know that the internal network is (192.168.1.0/24). This means that we will set the source IP to that because we need the internal network for this function. Also, since we want those queries to reach the DNS server, we will set the action to "allow". 
</p>
<p> 
    🛡️The fourth question wants SMTPS traffic to reach the mail server. This question asks us what the destination IP address is and on what port number. Since the question states that the mail server is (10.0.0.4), we will set it to that. As well as setting the port number to 587 for SMTPS traffic to flow. It is not port 25 because that would be SMTP, the insecure version. 
</p>
<p> 
    🛡️Lastly, we want to deny all the other traffic by default. In this case, we can simply set the destination IP to "any" and the port number to "any". This is because we already set the action to "deny", where anything that comes in that's not in rule 1,2,3, and 4, will get denied. 
</p>
