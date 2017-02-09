# Feed-The-Beast Presents HermitPack (Minecraft 1.10.2) in a Docker Container
To pull the image:
```
docker pull audiohacked/ftb_hermitpack_110:stable
```

It's highly recommended run a data container:
```
docker run --name ftb_hermitpack_datastore audiohacked/ftb_hermitpack_110:stable true
```

Then, run the server container:
```
docker run --detach --interactive --tty \
    --name ftb_hermitpack \
    --volumes-from ftb_hermitpack_datastore \
    -p 25565:25565 \
    -e EULA=TRUE \
    audiohacked/ftb_hermitpack_110:stable
```
