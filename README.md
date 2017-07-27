# Feed-The-Beast Presents HermitPack (Minecraft 1.10.2) in a Docker Container
To pull the image:
```
docker pull audiohacked/ftb_hermitpack_110:stable
```

It's highly recommended run a named data volume:
```
docker volume create minecraft_ftb_hermitpack_data
```

Then, run the server container:
```
docker run --detach --interactive --tty \
    --name ftb_hermitpack \
    --volume minecraft_ftb_hermitpack_data:/minecraft/world \
    --publish 25565:25565 \
    --env EULA=TRUE \
    audiohacked/ftb_hermitpack_110:stable
```
