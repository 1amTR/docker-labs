# Hướng dẫn sử dụng

## Cài đặt Docker Compose

Cài đặt
```
sudo curl -L "https://github.com/docker/compose/releases/download/1.26.0/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

sudo chmod +x /usr/local/bin/docker-compose
```

## Chạy file `docker-compose.yml`

Bạn phải đang trong thư mục `wordpress-docker`

```
docker-compose up -d
```

Xóa và tắt Wordpress Docker

```
docker-compose down
```

## Sử dụng

- Copy toàn bộ source code vào trong thư mục `/htdocs`

- Xuất file database từ phpmyadmin của bạn. Đăng nhập vào phpmyadmin trên Wordpress Docker bằng `http://IP:8080` và nhập vào.

## Troubleshooting

Xem logs của các container

```
docker logs wordpress
docker logs phpmyadmin
docker logs database
```