# ansible-docker-registry
```
$ ansible-playbook --version
ansible-playbook 2.7.8
```

```
ansible-playbook -i ./hosts.yml ./site.yml -k
```
## 自己証明書設定(Mac)
Portusにイメージをpushするためにクライアントに作成した自己証明書を設定しなければならない。
Macの場合`~/.docker/certs.d/{FQDN}`ディレクトリを作成し自己証明書を配置する。

```
$ mkdir ~/.docker/certs.d/{FQDN}
$ cp ./portus.crt ~/.docker/certs.d/{FQDN}/ca.crt
```

dockerの再起動を行う。
