# Cài đặt Docker

## Cài Docker trên Ubuntu

- Gỡ cài đặt phiên bản cũ

```
sudo apt-get remove docker docker-engine docker.io containerd runc
```

- Cập nhật và cài đặt một số repo cần thiết

```
sudo apt-get update

sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
    software-properties-common
```

- Thêm GPG key Docker

```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```

- Kiểm tra kiến trúc Linux
  
```
cat /etc/os-release

sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"
```   

- Cài đặt Docker Engine

```
sudo apt-get update

sudo apt-get install docker-ce docker-ce-cli containerd.io -y
```

- Chạy hello-world image

```
sudo docker run hello-world
```

> Để không dùng sudo mỗi lần gõ docker, chúng ta phải thêm docker vào group 

```
sudo usermod -aG docker your-user
```

- Gỡ cài đặt

```
sudo apt-get purge docker-ce docker-ce-cli containerd.io

sudo rm -rf /var/lib/docker
```

*Tham khảo: https://docs.docker.com/engine/install/ubuntu/*

