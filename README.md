<!-- markdownlint-disable -->
![Infrahub Logo](https://assets-global.website-files.com/657aff4a26dd8afbab24944b/657b0e0678f7fd35ce130776_Logo%20INFRAHUB.svg)
<!-- markdownlint-restore -->

# Infrahub by OpsMill

[Infrahub](https://github.com/opsmill/infrahub) by [OpsMill](https://opsmill.com) acts as a central hub to manage the data, templates and playbooks that powers your infrastructure. At its heart, Infrahub is built on 3 fundamental pillars:

- **A Flexible Schema**: A model of the infrastructure and the relation between the objects in the model, that's easily extensible.
- **Version Control**: Natively integrated into the graph database which opens up some new capabilities like branching, diffing, and merging data directly in the database.
- **Unified Storage**: By combining a graph database and git, Infrahub stores data and code needed to manage the infrastructure.

## Infrahub - Demo repository for IXPs

This repository is demoing the key Infrahub features for an example service provider with IXP peerings.

## Running the demo on your pc

### Set environment variables

```console
export INFRAHUB_ADDRESS="http://localhost:8000"
export INFRAHUB_API_TOKEN="06438eb2-8019-4776-878c-0941b1f1d1ec"
```

### Install the Infrahub SDK

```console
poetry install --no-interaction --no-ansi --no-root
```

### Start Infrahub

```console
poetry run invoke start
```

### Load schema and data into Infrahub

This will create:

- Basic data (Account, organization, ASN, Device Type, and Tags)
- Location data (Locations, VLANs, and Prefixes)
- IXP data

```console
poetry run invoke load-schema load-data
```

### Stop and destroy the IXP demo environment

```console
invoke destroy
```

## Using Github CodeSpaces

[Spin up in Github codespace](https://codespaces.new/opsmill/infrahub-demo-ixp)
