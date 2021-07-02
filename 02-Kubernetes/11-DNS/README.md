```
root@ip-172-31-3-195:~/docker-k8s-23-June-2021/02-Kubernetes/11-DNS# kubectl exec -it busybox -- sh
/ #
/ #
/ # cat /etc/resolv.conf
nameserver 10.96.0.10
search default.svc.cluster.local svc.cluster.local cluster.local us-east-2.compute.internal
options ndots:5
/ #
/ #
/ # nslookup kubernetes
Server:    10.96.0.10
Address 1: 10.96.0.10

nslookup: can't resolve 'kubernetes'
/ #
/ # nslookup wordpress-service
Server:    10.96.0.10
Address 1: 10.96.0.10

nslookup: can't resolve 'wordpress-service'
/ #
/ #
/ #
/ #
/ #
/ # nslookup wordpress-service
Server:    10.96.0.10
Address 1: 10.96.0.10

nslookup: can't resolve 'wordpress-service'
/ # di
diff     dirname
/ # di
diff     dirname
/ # di
diff     dirname
/ # nslookup 10.97.196.43
Server:    10.96.0.10
Address 1: 10.96.0.10 kube-dns.kube-system.svc.cluster.local

Name:      10.97.196.43
Address 1: 10.97.196.43 wordpress-service.default.svc.cluster.local
/ #
/ #
/ #
/ #
/ # nslookup wordpress-service.default.svc.cluster.local
Server:    10.96.0.10
Address 1: 10.96.0.10 kube-dns.kube-system.svc.cluster.local

Name:      wordpress-service.default.svc.cluster.local
Address 1: 10.97.196.43 wordpress-service.default.svc.cluster.local
/ #
/ #
/ #
/ #
/ #
/ # cat /etc/resolv.conf
nameserver 10.96.0.10
search default.svc.cluster.local svc.cluster.local cluster.local us-east-2.compute.internal
options ndots:5
/ # nslookup default-subdomain.svc.cluster.local
Server:    10.96.0.10
Address 1: 10.96.0.10 kube-dns.kube-system.svc.cluster.local

nslookup: can't resolve 'default-subdomain.svc.cluster.local'
/ # nslookup busybox-1.default-subdomain.svc.cluster.local
Server:    10.96.0.10
Address 1: 10.96.0.10 kube-dns.kube-system.svc.cluster.local

nslookup: can't resolve 'busybox-1.default-subdomain.svc.cluster.local'
/ # nslookup busybox-1.default-subdomain.svc.cluster.local
Server:    10.96.0.10
Address 1: 10.96.0.10 kube-dns.kube-system.svc.cluster.local

nslookup: can't resolve 'busybox-1.default-subdomain.svc.cluster.local'
/ # nslookup 192.168.185.220
Server:    10.96.0.10
Address 1: 10.96.0.10 kube-dns.kube-system.svc.cluster.local

Name:      192.168.185.220
Address 1: 192.168.185.220 busybox-1.default-subdomain.default.svc.cluster.local
/ # nslookup 192.168.238.225
Server:    10.96.0.10
Address 1: 10.96.0.10 kube-dns.kube-system.svc.cluster.local

Name:      192.168.238.225
Address 1: 192.168.238.225 busybox-2.default-subdomain.default.svc.cluster.local
/ # nslookup 192.168.185.219
Server:    10.96.0.10
Address 1: 10.96.0.10 kube-dns.kube-system.svc.cluster.local

Name:      192.168.185.219
Address 1: 192.168.185.219 ip-192-168-185-219.us-east-2.compute.internal
/ #
/ # nslookup 192.168.238.225
Server:    10.96.0.10
Address 1: 10.96.0.10 kube-dns.kube-system.svc.cluster.local

Name:      192.168.238.225
Address 1: 192.168.238.225 busybox-2.default-subdomain.default.svc.cluster.local
/ #
/ #
/ #
/ #
/ # nslookup busybox-2.default-subdomain.default.svc.cluster.local
Server:    10.96.0.10
Address 1: 10.96.0.10 kube-dns.kube-system.svc.cluster.local

Name:      busybox-2.default-subdomain.default.svc.cluster.local
Address 1: 192.168.238.225 busybox-2.default-subdomain.default.svc.cluster.local
/ #
/ #
/ #
/ # nslookup busybox-1.default-subdomain.default.svc.cluster.local
Server:    10.96.0.10
Address 1: 10.96.0.10 kube-dns.kube-system.svc.cluster.local

nslookup: can't resolve 'busybox-1.default-subdomain.default.svc.cluster.local'
/ # nslookup 192.168.185.220
Server:    10.96.0.10
Address 1: 10.96.0.10 kube-dns.kube-system.svc.cluster.local

Name:      192.168.185.220
Address 1: 192.168.185.220 busybox-1.default-subdomain.default.svc.cluster.local
/ # nslookup busybox-1.default-subdomain.default.svc.cluster.local
Server:    10.96.0.10
Address 1: 10.96.0.10 kube-dns.kube-system.svc.cluster.local

Name:      busybox-1.default-subdomain.default.svc.cluster.local
^C
/ # cat /etc/resolv.conf
nameserver 10.96.0.10
search default.svc.cluster.local svc.cluster.local cluster.local us-east-2.compute.internal
options ndots:5
/ #
/ # cat /etc/resolv.conf
nameserver 10.96.0.10
search default.svc.cluster.local svc.cluster.local cluster.local us-east-2.compute.internal

```
