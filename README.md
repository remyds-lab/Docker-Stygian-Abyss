


## Construir imagen

Creando
``` bash
mkdir stygian-abyss-docker
cd stygian-abyss-docker
```


``` bash
git clone https://github.com/jucarave/Stygian-Abyss.git
```

``` bash
docker build --no-cache -t stygian-abyss .
```

``` bash
docker run -d -p 8080:80 --name stygian-abyss-game stygian-abyss
```

- http://localhost:8080          página principal
- http://localhost:8080/play     redirige al juego
- http://localhost:8080/stygian/ juego directo

``` bash
docker stop stygian-abyss-game
docker rm stygian-abyss-game
```



``` bash
docker login -u remyds
```

``` bash
docker tag stygian-abyss remyds/stygian-abyss:latest
docker tag stygian-abyss remyds/stygian-abyss:v2.0
```

``` bash
docker push remyds/stygian-abyss:latest
docker push remyds/stygian-abyss:v2.0
```

