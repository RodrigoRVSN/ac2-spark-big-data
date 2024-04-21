# Como rodar 

- Rodar Makefile para buildar os containers do docker

> make -f Makefile

- Rode o docker compose

> docker-compose up -d

- Copie o CSV dentro do spark master

> docker cp user_data/Combined_Flights_2022.csv spark-master:/user_data

- Entre no container

> docker exec -it spark-master /bin/bash

- Crie no HDFS a pasta em que o dataset será salvo

> hadoop fs -mkdir /datasets/flight

- Salve o dataset do docker na pasta criada dentro do HDFS

> hadoop fs -put /user_data/Combined_Flights_2022.csv /datasets/flight

# Referências
- Mais informações em https://github.com/gbieul/spyrk-cluster 
