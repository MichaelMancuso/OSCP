# OSCP

# A few tips for OSCP

1. Doing all of the exercises is important since you will discover low-hanging fruit from the labs based on the recon you do with the different tools in the exercises.
2. Be wary of doing full /24 range port scans, especially for anything more than a few TCP ports. The machines might be in all sorts of broken states left by students etc.
3. When starting to recon a specific machine:
- Revert
- Port scan
- Try to identify services

Those steps in that order are important. You want a fresh state for the machine and you want to do just simple port scanning first because doing nmap's service scanning or nse scripts might send payloads that actually crash services. So be careful.

My recommendation for attacking the network: choose a protocol you feel you could easily test to see if it vulnerable and then scan for that in the public /24. Then choose one of them, repeat steps above to get a 100% confident read on whether that service is really running and what version => find exploits => try to exploit. This usually is not as easy as that, so try to see if you can exfiltrate some more intel about the server -- passwd file, keys, configuration data that helps you attack it in some other way.

Hope this helps.

JW

---
Further reading -> https://gist.github.com/unfo/5ddc85671dcf39f877aaf5dce105fac3
