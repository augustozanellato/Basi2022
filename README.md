# Basi di Dati A.A. 2021/2022

Semplice ambiente docker-compose contenente tutto il necessario per seguire i laboratori del corso Basi di Dati tenuto presso UniPD nell'anno accademico 2021/2022.

## Software installati
 - Postgresql 14.x (per comodità viene fissata solo la major version in modo da ricevere facilmente eventuali bugfix)
 - Pgadmin4 6.x (come sopra)

## Requisiti:
 - Docker
 - `docker-compose`

## Configurazione
Prima del primo avvio è necessario copiare `.env.sample` in `.env` e modificare i seguenti parametri:
 - `POSTGRES_USER`: nome utente creato al primo avvio
 - `POSTGRES_PASSWORD`: password dell'utente di cui sopra
 - `POSTGRES_DB`: nome del database creato di default

## Esecuzione
```sh
docker-compose up -d
```
**Nota: è normale che Pgadmin non sia raggiungibile per i primi ~30 secondi dall'avvio.**

Dopo l'esecuzione del comando di cui sopra Pgadmin sarà raggiungibile a http://localhost:8080/, mentre Postgresql sarà accessibile sulla porta 5432 (**nota: sarà accessibile solo da localhost**).

## Aggiornamento
```sh
docker-compose pull
```

## Reset ad uno stato pulito
```sh
docker-compose down -v
```

## NOTA
Questo progetto non è pensato per l'uso in produzione ma solo per test locali, non sono stati infatti presi in considerazione aspetti di sicurezza o performance.
