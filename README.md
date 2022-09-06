# docker-alpine-openrc

Alpine Linux funcionando con Systemd (service x start | restart) (rc-service add x | rc-service del x)
Recomendado para ejecutar varios servicios dentro de un solo contenedor, gracias a openrc solo instala el servicio y con rc-service add x && service x start.

## Compilar
```sh
docker build -t alpine-openrc .
```

## Ejecutar
```sh
docker run  -it -d --tty  --privileged  --volume /sys/fs/cgroup:/sys/fs/cgroup:ro --name alpine-openrc alpine-openrc
```

## Ejecutar y que inicie automáticamente
```sh
docker run  -it -d --restart always --tty  --privileged  --volume /sys/fs/cgroup:/sys/fs/cgroup:ro --name alpine-openrc alpine-openrc
```
