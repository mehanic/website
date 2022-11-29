---
title: "Long Page Title"
linkTitle: "Short Nav Title"
weight: 100
description: >-
     Page description for heading and indexes.
---

## Heading

Edit this template to create your new page.

* Give it a good name, ending in `.md` - e.g. `getting-started.md`
* Edit the "front matter" section at the top of the page (weight controls how its ordered amongst other pages in the same directory; lowest number first).
* Add a good commit message at the bottom of the page (<80 characters; use the extended description field for more detail).
* Create a new branch so you can preview your new file and request a review via Pull Request.

root@controlplane ~ ➜  alias k=kubectl

root@controlplane ~ ➜  ETCDCTL_API=3 etcdctl --endpoints https://127.0.0.1:2379 \
> ^C

root@controlplane ~ ✖ ETCDCTL_API=3 etcdctl --cacert="/etc/kubernetes/pki/etcd/ca.crt" --cert="/etc/kubernetes/pki/etcd/server.crt" --key="/etc/kubernetes/pki/etcd/server.key" snapshot save /opt/snapshot-pre-boot.dbSnapshot saved at /opt/snapshot-pre-boot.db

root@controlplane ~ ➜  k get all
NAME                 TYPE        CLUSTER-IP   EXTERNAL-IP   PORT(S)   AGE
service/kubernetes   ClusterIP   10.96.0.1    <none>        443/TCP   7s

root@controlplane ~ ➜  ETCDCTL_API=3 etcdctl --cacert="/etc/kubernetes/pki/etcd/ca.crt" --cert="/etc/kubernetes/pki/etcd/server.crt" --key="/etc/kubernetes/pki/etcd/server.key" --data-dir="/var/lib/etcd-from-backup" snapshot restore /opt/snapshot-pre-boot.db
2022-07-09 12:10:34.640762 I | mvcc: restore compact to 2731
2022-07-09 12:10:34.648279 I | etcdserver/membership: added member 8e9e05c52164694d [http://localhost:2380] to cluster cdf818194e3a8c32

