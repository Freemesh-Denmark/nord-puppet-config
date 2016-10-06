# Install scripts for the Freemesh Denmark Gateway

### 1. copy this file to the root home folder:

```
cp mesh_peerings.yaml /root/
```

### 2. create the file with the fastd private key

```
echo 'secret "xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx";' > /root/fastd_secret.key
```

#### 3. start the pre, puppet and post stcript

```
./pre-puppet.sh
(follow instructions at the end of the script)
puppet apply --verbose manifest.pp
build-firewall
/post-puppet.sh
```
