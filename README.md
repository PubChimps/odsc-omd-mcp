# AI Driven Automation in Open-Source Metadata Platforms: Embedding an MCP Server

Hello Open Data Science Conference! Thank you for joining our training session! You can find the contents below, please let me know if there's anything you need!

*Note - This training was prepared using a MacBook*

## Contents
1. Prerequisites
2. OpenMetadata
3. Adding the OpenMetadata MCP Server to goose
4. Prompt party! 🎉
5. goose Recipes
6. Wrapping up and feedback

## Prerequisites
Before getting started, please make sure you have the following two services on your laptop:
1. [Docker Desktop](https://www.docker.com/products/docker-desktop/) - there are open-source alternatives to Docker, like Podman, that are great, please do not use them for this workshop!
2. [goose Desktop](https://block.github.io/goose/docs/quickstart/) - Desktop, not goose CLI

## OpenMetadata
With the prerequisites installed, we will move on to installing OpenMetadata. OpenMetadata is an open-source metadata platform for data discovery, observability and governance! If you have any questions about OpenMetadata, please ask! We will be installing OpenMetadata along with its supporting components:

 * Airflow - Which orchestrates ingestion jobs that bring new metadata into OpenMetadata, keep it up to data as data systems change
 * Elasticsearch - Search indexing to retrieve OpenMetadata assets
 * PostgreSQL - Stores and maintain state for OpenMetadata assets

We'll bring all these services online with the following commands:

```
curl -sL -o docker-compose-postgres.yml https://github.com/open-metadata/OpenMetadata/releases/download/1.10.2-release/docker-compose-postgres.yml
wget https://github.com/open-metadata/OpenMetadata/releases/download/1.10.2-release/docker-compose-postgres.yml
curl -fsSL https://raw.githubusercontent.com/open-metadata/openmetadata-demo/main/postgres/docker/postgres-script.sql | docker exec -i openmetadata_postgresql psql -U postgres -d openmetadata_db
```

## Adding the OpenMetadata MCP Server to goose

## Prompt party! 🎉

## goose Recipes

## Wrapping up and feedback
To shutdown your OpenMetadata services, run the following command:

```
docker compose down
```

Or, you can add additional metadata connectors to your OpenMetadata instance! Popular connectors include Snowflake, BigQuery, Databricks, and Tableau!
