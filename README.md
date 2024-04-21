# Como rodar 

- Rodar Makefile para buildar os containers do docker

```bash
make -f Makefile
```

Rode o docker compose

```bash
docker-compose up -d
```

- Copie o CSV dentro do spark master

```bash
docker cp user_data/Combined_Flights_2022.csv spark-master:/user_data
```

- Entre no container

```bash
docker exec -it spark-master /bin/bash
```

- Crie no HDFS a pasta em que o dataset será salvo

```bash
hadoop fs -mkdir /datasets/flight
```

- Salve o dataset do docker na pasta criada dentro do HDFS

```bash
hadoop fs -put /user_data/Combined_Flights_2022.csv /datasets/flight
```

# Referências
- Mais informações em https://github.com/gbieul/spyrk-cluster 
