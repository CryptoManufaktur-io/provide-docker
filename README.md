# provide-docker

docker-compose for provide stack

## Installing prereqs

Assuming Ubuntu, and if you don't already have docker.io or docker-ce installed:
`sudo apt install git docker.io docker-compose`

Optional:
`sudo -aG docker MYUSER && newgrp docker`

> Caution: There have been reports of data loss with Ubuntu Desktop's docker snap package,
> caused by it changing the location of the volumes on update of the package. Don't use the docker snap package,
> use one of the apt packages instead.

## Use

To use: Follow instructions at https://docs.provide.services/api/quickstart/baseledger-running-a-node/running-a-node using `docker-compose run cli`. `exit` when done.

Then `cp default.env .env`, and `nano .env` and add the Vault ID, Vault Key ID and Refresh Token.

Then start the node: `docker-compose up -d node`

Observing the logs: `docker-compose logs -f node`
