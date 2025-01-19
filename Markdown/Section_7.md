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
    🛡️In the first question, we set the source IP address for rule 1 to "any." This is because the question specifies that HTTP and HTTPS traffic from any external IP address should be allowed to reach the web server. Since we are dealing with port 80, which corresponds to HTTP, we will set the action to "allow" to enable the traffic to reach the web server.
</p>
<p>
    For rule 2, as we are dealing with HTTPS traffic on port 443, we need to set the destination IP address to (10.0.0.1), which is the IP address of the web server.
</p>
<p> 
    🛡️In the second question, we need to allow SSH traffic from the internal network to the database server, as the question specifies the required port number. Since SSH operates on port 22, we will configure the rule to allow traffic on that port. 
</p>
<p>
    🛡️Next, we need to allow DNS queries from any device on the internal network to the DNS server. Based on question 2 and the firewall rules, we know the internal network is (192.168.1.0/24). Therefore, we will set the source IP to (192.168.1.0/24) to allow this function. Additionally, since the queries are intended to reach the DNS server, we will set the action to "allow."
</p>
<p> 
    🛡️The fourth question requires us to configure SMTPS traffic to reach the mail server. It asks for the destination IP address and the port number. Since the mail server is (10.0.0.4), we will set the destination IP to this address. For the port number, we will use 587 for SMTPS traffic, as this is the secure version of SMTP. Port 25 would correspond to SMTP, which is insecure.
</p>
<p> 
    🛡️We want to deny all other traffic by default. To accomplish this, we will set the destination IP to "any" and the port number to "any." With the action set to "deny," any traffic not covered by rules 1, 2, 3, or 4 will be blocked.
</p>
