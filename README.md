# Project 9 - Honeypot

Time spent: **10** hours spent in total

> Objective: Setup a honeypot and intercept some attempted attacks in the wild

## Result

- Type of Honeypot Deployed: Dionaea
- Summary:
  - Total Attack(s): 19760
  - Total Malware(s): 1
- GIF Walkthrough: ![Live Capture](/capture/live_capture.gif)

## Issues Faced

- Very first challenge I faced was to load MHN admin in browser from external network. I had to modify VPN Firewall Rule of GCP to allow http traffic from external network.
- I found my sensor was detecting lots of attack but was not detecting any payload at all. So, no malware was being captured. After experimenting a while, I found port 445 needs to be accessible from outside network to be able to successfully upload a malware which was not. Then, to check for internal network, I have uploaded a malware with metaspoilt from internal network and it was captured by sensor. I couldn't figure out how to make port 445 accsible from external network.

