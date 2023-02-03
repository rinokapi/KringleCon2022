# 2022 SANS Holiday Hack Challenge & KringleCon
Join the global cybersecurity community in its most festive cyber security challenge and virtual conference of the year. The SANS Holiday Hack Challenge is a FREE series of super fun, high-quality, hands-on cybersecurity challenges. The SANS Holiday Hack Challenge is for all skill levels, with a stellar prize at the end for the best of the best entries.

https://www.sans.org/mlp/holiday-hack-challenge/

## Recover the Tolkien Ring ✔️
Recover the Elfen Ring.

### Wireshark Practice
Use the Wireshark Phishing terminal in the Tolkien Ring to solve the mysteries around the suspicious PCAP. Get hints for this challenge by typing hint in the upper panel of the terminal.

Challenges:
1. answer: ```http```, how?: ```wireshark export object```
2. answer: ```app.php```, how?:	```tsark -r pcap_challenge.pcap --export-objects http,newFolder```
3. answer: ```687```, how?: ```tsark -r pcap_challenge.pcap --export-objects http,newFolder | grep (text/html)```
4. answer: ```192.185.57.242```, how?: ```tsark -r pcap_challenge.pcap --export-objects http,newFolder | grep (text/html)```
5. answer: ```Ref_Sept24-2020.zip```, how?: ```cat newFolder/app\(1\).php | grep zip```
6. answer: ```id-at-countryName=IL and id-at-countryName=SS```, how?: ```tls certificate issuer```
7. answer: ```yes```, how?: ```status code 200 on app.php thats has .zip download request```

### Windows Event Logs
Investigate the Windows event log mystery in the terminal or offline. Get hints for this challenge by typing hint in the upper panel of the Windows Event Logs terminal.

Challenges:
1. answer: ```12/24/2022```, how?: ```head powershell.evtx.log```
2. answer: ```Recipe```, how?: ```grep txt powershell.evtx.log```
3. answer: ```$foo = Get-Content .\Recipe| % {$_ -replace 'honey', 'fish oil'}```
4. answer: ```$foo | Add-Content -Path 'Recipe'```
5. answer: ```Recipe.txt```
6. answer: ```yes```, how?: ```at line 6568 and line 6762 in the log with command "grep Recipe powershell.evtx.log -ni"```
7. answer: ```no```, how?: ```nothing in the log "del .\Recipe", only "del .\Recipe.txt"```
8. answer: ```4104```, how?: ```$foo = Get-Content .\Recipe| % {$_ -replace 'honey', 'fish oil'} $foo | Add-Content -Path 'reci pe_updated.txt'```
9. answer: ```yes```
10. answer: ```honey, fish oil```

### Suricata Regatta
Help detect this kind of malicious activity in the future by writing some Suricata rules. Work with Dusty Giftwrap in the Tolkien Ring to get some hints.

Challenges:

1. Please create a Suricata rule to catch DNS lookups for adv.epostoday.uk. Whenever there's a match, the alert message (msg) should read Known bad DNS lookup, possible Dridex infection. Answer: ```alert dns any any -> any any (msg:"Known bad DNS lookup, possible Dridex infection"; dns.query; content:"adv.epostoday.uk"; nocase;)```
2. STINC thanks you for your work with that DNS record! In this PCAP, it points to 192.185.57.242. Develop a Suricata rule that alerts whenever the infected IP address 192.185.57.242 communicates with internal systems over HTTP. When there's a match, the message (msg) should read Investigate suspicious connections, possible Dridex infection. Answer: ```alert http 192.185.57.242 any <> $HOME_NET any (msg:"Investigate suspicious connections, possible Dridex infection"; sid:1;)```
3. We heard that some naughty actors are using TLS certificates with a specific CN. Develop a Suricata rule to match and alert on an SSL certificate for heardbellith.Icanwepeh.nagoya. When your rule matches, the message (msg) should read Investigate bad certificates, possible Dridex infection. Answer: ```alert tls any any -> any any (msg:"Investigate bad certificates, possible Dridex infection"; tls.cert_subject; content:"CN=heardbellith.Icanwepeh.nagoya"; isdataat:!1,relative;)```
4. OK, one more to rule them all and in the darkness find them. Let's watch for one line from the JavaScript: let byteCharacters = atob. Oh, and that string might be GZip compressed - I hope that's OK! Just in case they try this again, please alert on that HTTP data with message Suspicious JavaScript function, possible Dridex infection. Answer: ```alert http any any -> any any (msg:"Suspicious JavaScript function, possible Dridex infection"; file_data; content:"let byteCharacters = atob";)```

## Recover the Elfen Ring ❌
Recover the Elfen Ring.

### Clone with a Difference
Clone a code repository. Get hints for this challenge from Bow Ninecandle in the Elfen Ring.

Challenges:

## Recover the Web Ring ❌
Recover the Web Ring.

### Naughty IP
Use the artifacts from Alabaster Snowball to analyze this attack on the Boria mines. Most of the traffic to this site is nice, but one IP address is being naughty! Which is it? Visit Sparkle Redberry in the Tolkien Ring for hints.

Challenges: 

### Credential Mining
The first attack is a brute force login. What's the first username tried?

Challenges: 

### 404 FTW
The next attack is forced browsing where the naughty one is guessing URLs. What's the first successful URL path in this attack?

Challenges: 

### IMDS, XXE, and Other Abbreviations
The last step in this attack was to use XXE to get secret keys from the IMDS service. What URL did the attacker force the server to fetch?

Challenges: 

## Recover the Cloud Ring ❌
Recover the Cloud Ring.

### AWS CLI Intro
Try out some basic AWS command line skills in this terminal. Talk to Jill Underpole in the Cloud Ring for hints.

Challenges:

## Recover the Burning Ring of Fire ❌
Recover the Burning Ring of Fire.

### Buy a Hat
Travel to the Burning Ring of Fire and purchase a hat from the vending machine with KringleCoin. Find hints for this objective hidden throughout the tunnels.

Challenges:
