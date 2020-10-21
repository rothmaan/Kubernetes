# Kubernetes


Kubernetes on Linux containers


Multi-node kubernetes cluster on LXD/LXC.

<br />
vagrant@k8s:~$ lxc list
+--------------+---------+-------------------+------+------------+-----------+\
|     NAME     |  STATE  |       IPV4        | IPV6 |    TYPE    | SNAPSHOTS |\
+--------------+---------+-------------------+------+------------+-----------+\
| controller-0 | RUNNING | 10.0.2.10 (eth1)  |      | PERSISTENT | 0         |\
|              |         | 10.0.1.155 (eth0) |      |            |           |\
+--------------+---------+-------------------+------+------------+-----------+\
| controller-1 | RUNNING | 10.0.2.11 (eth1)  |      | PERSISTENT | 0         |\
|              |         | 10.0.1.31 (eth0)  |      |            |           |\
| controller-2 | RUNNING | 10.0.2.12 (eth1)  |      | PERSISTENT | 0         |\
|              |         | 10.0.1.225 (eth0) |      |            |           |\
+--------------+---------+-------------------+------+------------+-----------+\
| haproxy      | RUNNING | 10.0.1.100 (eth0) |      | PERSISTENT | 0         |\
+--------------+---------+-------------------+------+------------+-----------+\
| worker-0     | RUNNING | 10.0.2.20 (eth1)  |      | PERSISTENT | 0         |\
|              |         | 10.0.1.178 (eth0) |      |            |           |\
+--------------+---------+-------------------+------+------------+-----------+\

<br />

<br />
vagrant@k8s:~$ kubectl get nodes -owide
<br />
NAME       STATUS   ROLES    AGE   VERSION   INTERNAL-IP   EXTERNAL-IP   OS-IMAGE             KERNEL-VERSION       CONTAINER-RUNTIME
<br />
worker-0   Ready    <none>   85d   v1.18.0   10.0.1.178    <none>        Ubuntu 18.04.4 LTS   4.15.0-112-generic   containerd://1.2.10
<br />
worker-1   Ready    <none>   85d   v1.18.0   10.0.1.226    <none>        Ubuntu 18.04.4 LTS   4.15.0-112-generic   containerd://1.2.10
<br />
worker-2   Ready    <none>   85d   v1.18.0   10.0.1.223    <none>        Ubuntu 18.04.4 LTS   4.15.0-112-generic   containerd://1.2.10
<br />
vagrant@k8s:~$
<br />

