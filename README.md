Containerized `kube-apiserver` lb with `haproxy`

```
docker run --name haproxy -p 9000:9000 -p 6443:6443 --add-host api1:<KUBE-IP-1> --add-host api2:<KUBE-IP-2> --add-host api3:<KUBE-IP-3> -d chadmoon/kube-apiserver-haproxy:latest
```