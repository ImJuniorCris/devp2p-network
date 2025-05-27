# Devp2pNetwork

**About:**  
Monitor and record Ethereum DevP2P peer and network metrics in a database, and visualize them through an analytics dashboard.

## Overview

Devp2pNetwork is a monitoring tool for the Ethereum DevP2P network. It connects to Ethereum nodes using the DevP2P protocol, gathers peer/network statistics, stores this data in PostgresDB, and visualizes the results via Metabase.

![devp2p-network-screencap](https://user-images.githubusercontent.com/1383412/50279407-6c982e80-03fe-11e9-9156-09a6567dda06.png)

## Features

- Monitors Ethereum DevP2P network peers and connections.
- Records peer data and network metrics to a Postgres database.
- Provides a dashboard for analytics and visualization via Metabase.
- Docker and Docker Compose support for easy setup.
- Configurable for different Ethereum networks.

## Getting Started

1. **Install Node dependencies:**
   ```bash
   npm install
   ```

2. **Start database and dashboard backend services:**
   ```bash
   docker-compose up --detach
   ```

3. **Run the DevP2P monitor:**
   ```bash
   npm start
   ```

   It may take a minute for the client to connect to DevP2P peers. Once connected, peer data is saved to MongoDB/Postgres and can be visualized in Metabase.

4. **Access the dashboard:**
   Open [http://localhost:3000](http://localhost:3000) in your browser.

   You will need to configure Metabase by creating a user account and adding the Postgres connection info.

## Configuration

- Configuration can be set via a config file or command-line arguments.
- To use a custom network config:
  ```bash
  node index.js -c customNetwork.json
  ```
- To use a default Ethereum testnet:
  ```bash
  node index.js -n goerli
  ```

## License

Licensed under the [Apache License 2.0](LICENSE.md).

---

**Short About Section:**  
Monitor and record Ethereum DevP2P network peer metrics and visualize them using an analytics dashboard.
