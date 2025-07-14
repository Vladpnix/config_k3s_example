```
/etc/hosts
192.168.88.53   master.vlad.local   master
```
```
sudo hostnamectl hostname master.vlad.local
```
```
sudo nano /etc/network/interfaces
```
```
iface enp1s0 inet static
address 192.168.88.53
netmask 255.255.255.0
gateway 192.168.88.1
```

/etc/resolv.conf
```
nameserver 192.168.88.1
```
```
apt install apt-transport-https ca-certificates curl iptables
```
```
swapoff -a
```
https://it-tools.tech/token-generator?length=37

```
k3s_token="W28oK5s3ouZHWOyawkH4M6h0s1RF54rHKHLuC"
```
example install k3s
```
curl -sfL https://get.k3s.io | K3S_TOKEN=W28oK5s3ouZHWOyawkH4M6h0s1RF54rHKHLuC sh -s - server --cluster init
```
```
curl -sfL https://get.k3s.io | INSTALL_K3S_EXEC="server" sh -s - --flannel-backend none --token 12345
```
```
curl -sfL https://get.k3s.io | INSTALL_K3S_EXEC="server --flannel-backend none" K3S_TOKEN=12345 sh -s -
```
```
curl -sfL https://get.k3s.io | K3S_TOKEN=12345 sh -s - server --flannel-backend none
```
server is assumed below because there is no K3S_URL
```
curl -sfL https://get.k3s.io | INSTALL_K3S_EXEC="--flannel-backend none --token 12345" sh -s - 
```
```
curl -sfL https://get.k3s.io | sh -s - --flannel-backend none --token 12345
```
