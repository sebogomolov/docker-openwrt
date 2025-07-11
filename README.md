## Сборка Openwrt в Docker

В примере использован Debian 10 (Buster).

```bash
git clone https://github.com/sebogomolov/docker-openwrt.git
cd docker-openwrt
docker build -t openwrt_builder .
```

Создайте папку в которую будут собираться образы openwrt и соедините ее с docker-контейнером:

```bash
mkdir ~/build
docker run -v ~/build:/home/user:z -it openwrt_builder /bin/bash
```