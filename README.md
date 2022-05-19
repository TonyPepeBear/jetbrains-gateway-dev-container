# SSH Dev Container

Simple Container with SSH server and several development packages.

可以用 ssh 連入的容器，並已安裝基礎開發套件。

## Simple use (簡單使用)

```shell
docker pull ghcr.io/tonypepebear/ssh-dev-ubuntuc
docker run -d -p 8000:22 ghcr.io/tonypepebear/ssh-dev-ubuntuc
ssh -p 8000 ubuntu@localhost
```

The container's user name and password is both `ubuntu`.

容器的使用者和密碼都是 `ubuntu`。

## Container 容器

### Simple Ubuntu (最簡單的 Ubuntu)

Installed packages: openssh-server ssh sudo git vim

已經安裝的套件: openssh-server ssh sudo git vim
