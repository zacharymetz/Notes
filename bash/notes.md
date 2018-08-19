# 7/9/2018
### set the DNS server of ubuntu to googles DNS if you cannot connect to hostnames
8.8.8.8 is google and 1.1.1.1 is cloudflare incase one is down
```
echo "nameserver 8.8.8.8" | sudo tee /etc/resolv.conf
```

# 5/7/2018
### How to generate junk files of n MB in size 
this example generates a 24MB file
```
fallocate -l 24M filename
```

# 8/19/2018
### whats my ip
```
wget http://ipecho.net/plain -O - -q ; echo
```
