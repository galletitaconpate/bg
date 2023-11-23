# Bug Bounty Personal Tips

``` assetfinder X.com | tee -a /tmp/X.txt```

``` cat /tmp/X.txt | httprobe -p http:81 -p https:8443 -p http:8000 -p http:8001 -p http:8181 -t 40000 | tee -a /tmp/X.txt ```

``` nuclei -l /tmp/X.txt -t cves. -t default-credentials/ -o /tmp/X_results.txt```
