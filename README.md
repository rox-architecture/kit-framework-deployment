# KIT framework deployment

Information and user manual: https://rox-architecture.github.io/kit-user-manual/

## System Components

The overall KIT framework consists of the following container images:
- **kit-backend**: for backend-api and backend-worker instances
- **kit-backend-db**: database that stores previously used KITs and their execution history
- **kit-backend-redis**: message passing between worker instances
- **kit-frontend**: graphical user interface to edit/trigger KITs
- **local-federated-catalog-dlr**: locally running federated catalog to fetch all the assets you can see in DLR dataspace

Note: 
- Later, we will also add **local-federated-catalog-ts**
- Multiple worker instances up to 4 can be spawned, and can be deployed on different machines

## Run with GUI

```bash
docker compose --profile gui pull
docker compose --profile gui up -d
```

## Run without GUI (headless)

```bash
docker compose pull
docker compose up -d
```

## Funding

This open-source project was developed within the *[ROX](https://www.project-rox.ai/en/)* project. 
This project has received public funding from the **European Union** NextGenerationEU within the Important Project of Common European Interest – Cloud Infrastructures and Services (IPCEI-CIS) under grant agreement 13IPC034.

<p align="center">
  <img alt="Bundesministerium für Wirtschaft und Energie (BMWE)-EU and secunet funding logo" src="bmwe_logo.png" width="400"/>
</p>
