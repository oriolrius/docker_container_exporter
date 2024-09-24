
# docker_container_exporter

A Prometheus exporter that collects metrics about Docker containers. The exporter is written in Python and uses the Docker SDK to interact with the Docker API.

The exporter exposes the following metrics:

- `docker_containers_total`: Total number of Docker containers
- `docker_containers_running_total`: Number of running Docker containers
- `docker_containers_stopped_total`: Number of stopped Docker containers
- `docker_containers_other_total`: Number of Docker containers in other states (not running or stopped)

## Table of contents

- [Requirements](#requirements)
- [Development](#development)
- [Running the Application](#running-the-application)
  - [Using Python](#using-python)
  - [Using Docker](#using-docker)
- [Configuration](#configuration)

## Requirements

- Docker
- Python 3.10
- Prometheus

## Development

1. **Clone the repository:**

    ```sh
    git clone git@github.com:oriolrius/docker_container_exporter.git
    cd docker_container_exporter
    ```

1. **Create and activate a virtual environment:**

    ```sh
    python3 -m venv venv
    source venv/bin/activate
    ```

1. **Install the dependencies:**

    ```sh
    pip install -r requirements.txt
    ```

1. **Configure the default port:**

    ```sh
    export PORT=9000
    ```

## Running the Application

### Using Python

1. **Run the application:**

    ```sh
    python containers_running.py
    ```

2. **Access the Prometheus metrics:**

    Open your browser and go to [`http://localhost:8118/metrics`](command:_github.copilot.openSymbolFromReferences?%5B%22http%3A%2F%2Flocalhost%3A8118%2Fmetrics%22%2C%5B%7B%22uri%22%3A%7B%22%24mid%22%3A1%2C%22fsPath%22%3A%22%2Fdocker-data%2Fcontainers_running%2Fcontainers_running.py%22%2C%22external%22%3A%22file%3A%2F%2F%2Fdocker-data%2Fcontainers_running%2Fcontainers_running.py%22%2C%22path%22%3A%22%2Fdocker-data%2Fcontainers_running%2Fcontainers_running.py%22%2C%22scheme%22%3A%22file%22%7D%2C%22pos%22%3A%7B%22line%22%3A21%2C%22character%22%3A44%7D%7D%2C%7B%22uri%22%3A%7B%22%24mid%22%3A1%2C%22fsPath%22%3A%22%2Fdocker-data%2Fcontainers_running%2Fvenv%2Flib%2Fpython3.10%2Fsite-packages%2Fdocker%2Fapi%2Fbuild.py%22%2C%22external%22%3A%22file%3A%2F%2F%2Fdocker-data%2Fcontainers_running%2Fvenv%2Flib%2Fpython3.10%2Fsite-packages%2Fdocker%2Fapi%2Fbuild.py%22%2C%22path%22%3A%22%2Fdocker-data%2Fcontainers_running%2Fvenv%2Flib%2Fpython3.10%2Fsite-packages%2Fdocker%2Fapi%2Fbuild.py%22%2C%22scheme%22%3A%22file%22%7D%2C%22pos%22%3A%7B%22line%22%3A143%2C%22character%22%3A31%7D%7D%2C%7B%22uri%22%3A%7B%22%24mid%22%3A1%2C%22fsPath%22%3A%22%2Fdocker-data%2Fcontainers_running%2Fvenv%2Flib%2Fpython3.10%2Fsite-packages%2Fsetuptools%2F_distutils%2Fcommand%2Fbdist_rpm.py%22%2C%22external%22%3A%22file%3A%2F%2F%2Fdocker-data%2Fcontainers_running%2Fvenv%2Flib%2Fpython3.10%2Fsite-packages%2Fsetuptools%2F_distutils%2Fcommand%2Fbdist_rpm.py%22%2C%22path%22%3A%22%2Fdocker-data%2Fcontainers_running%2Fvenv%2Flib%2Fpython3.10%2Fsite-packages%2Fsetuptools%2F_distutils%2Fcommand%2Fbdist_rpm.py%22%2C%22scheme%22%3A%22file%22%7D%2C%22pos%22%3A%7B%22line%22%3A416%2C%22character%22%3A47%7D%7D%2C%7B%22uri%22%3A%7B%22%24mid%22%3A1%2C%22fsPath%22%3A%22%2Fdocker-data%2Fcontainers_running%2Fvenv%2Flib64%2Fpython3.10%2Fsite-packages%2Fsetuptools%2F_distutils%2Fcommand%2Fbdist_rpm.py%22%2C%22external%22%3A%22file%3A%2F%2F%2Fdocker-data%2Fcontainers_running%2Fvenv%2Flib64%2Fpython3.10%2Fsite-packages%2Fsetuptools%2F_distutils%2Fcommand%2Fbdist_rpm.py%22%2C%22path%22%3A%22%2Fdocker-data%2Fcontainers_running%2Fvenv%2Flib64%2Fpython3.10%2Fsite-packages%2Fsetuptools%2F_distutils%2Fcommand%2Fbdist_rpm.py%22%2C%22scheme%22%3A%22file%22%7D%2C%22pos%22%3A%7B%22line%22%3A416%2C%22character%22%3A47%7D%7D%5D%5D "Go to definition").

### Using Docker

1. Get files `docker-compose.yml` and `.env` from the repository.

    ```sh
    wget https://raw.githubusercontent.com/oriolrius/docker_container_exporter/main/docker-compose.yml
    wget https://raw.githubusercontent.com/oriolrius/docker_container_exporter/main/.env
    ```

1. Edit them to set the desired configuration.

    ```sh
    nano .env
    nano docker-compose.yml
    ```

1. **Run the stack:**

    ```sh
    docker-compose up
    ```

1. **Access the Prometheus metrics:**

    Open your browser and go to [`http://localhost:8118/metrics`](command:_github.copilot.openSymbolFromReferences?%5B%22http%3A%2F%2Flocalhost%3A8118%2Fmetrics%22%2C%5B%7B%22uri%22%3A%7B%22%24mid%22%3A1%2C%22fsPath%22%3A%22%2Fdocker-data%2Fcontainers_running%2Fcontainers_running.py%22%2C%22external%22%3A%22file%3A%2F%2F%2Fdocker-data%2Fcontainers_running%2Fcontainers_running.py%22%2C%22path%22%3A%22%2Fdocker-data%2Fcontainers_running%2Fcontainers_running.py%22%2C%22scheme%22%3A%22file%22%7D%2C%22pos%22%3A%7B%22line%22%3A21%2C%22character%22%3A44%7D%7D%2C%7B%22uri%22%3A%7B%22%24mid%22%3A1%2C%22fsPath%22%3A%22%2Fdocker-data%2Fcontainers_running%2Fvenv%2Flib%2Fpython3.10%2Fsite-packages%2Fdocker%2Fapi%2Fbuild.py%22%2C%22external%22%3A%22file%3A%2F%2F%2Fdocker-data%2Fcontainers_running%2Fvenv%2Flib%2Fpython3.10%2Fsite-packages%2Fdocker%2Fapi%2Fbuild.py%22%2C%22path%22%3A%22%2Fdocker-data%2Fcontainers_running%2Fvenv%2Flib%2Fpython3.10%2Fsite-packages%2Fdocker%2Fapi%2Fbuild.py%22%2C%22scheme%22%3A%22file%22%7D%2C%22pos%22%3A%7B%22line%22%3A143%2C%22character%22%3A31%7D%7D%2C%7B%22uri%22%3A%7B%22%24mid%22%3A1%2C%22fsPath%22%3A%22%2Fdocker-data%2Fcontainers_running%2Fvenv%2Flib%2Fpython3.10%2Fsite-packages%2Fsetuptools%2F_distutils%2Fcommand%2Fbdist_rpm.py%22%2C%22external%22%3A%22file%3A%2F%2F%2Fdocker-data%2Fcontainers_running%2Fvenv%2Flib%2Fpython3.10%2Fsite-packages%2Fsetuptools%2F_distutils%2Fcommand%2Fbdist_rpm.py%22%2C%22path%22%3A%22%2Fdocker-data%2Fcontainers_running%2Fvenv%2Flib%2Fpython3.10%2Fsite-packages%2Fsetuptools%2F_distutils%2Fcommand%2Fbdist_rpm.py%22%2C%22scheme%22%3A%22file%22%7D%2C%22pos%22%3A%7B%22line%22%3A416%2C%22character%22%3A47%7D%7D%2C%7B%22uri%22%3A%7B%22%24mid%22%3A1%2C%22fsPath%22%3A%22%2Fdocker-data%2Fcontainers_running%2Fvenv%2Flib64%2Fpython3.10%2Fsite-packages%2Fsetuptools%2F_distutils%2Fcommand%2Fbdist_rpm.py%22%2C%22external%22%3A%22file%3A%2F%2F%2Fdocker-data%2Fcontainers_running%2Fvenv%2Flib64%2Fpython3.10%2Fsite-packages%2Fsetuptools%2F_distutils%2Fcommand%2Fbdist_rpm.py%22%2C%22path%22%3A%22%2Fdocker-data%2Fcontainers_running%2Fvenv%2Flib64%2Fpython3.10%2Fsite-packages%2Fsetuptools%2F_distutils%2Fcommand%2Fbdist_rpm.py%22%2C%22scheme%22%3A%22file%22%7D%2C%22pos%22%3A%7B%22line%22%3A416%2C%22character%22%3A47%7D%7D%5D%5D "Go to definition").

## Grafana Alloy

Using Grafana Alloy you can collect the metrics from the exporter and send a Promtheus compatiable server, for instance Grafana Mimir.

Of course, you can use Prometheus directly and any other Prometheus compatible agent.

Next you can see an example of the configuration for Alloy to collect the metrics from the exporter and send them to Grafana Mimir (metrics database compatible with Prometheus).

```config.alloy
prometheus.scrape "node_containers" {
  targets    = [
    { "__address__" = "localhost:8118",
      "__scheme__" = "http",
      "instance" = "iiot",
      "job" = "node_containers",
      "__scrape_interval__" = "10s",
     },
  ]
  forward_to = [prometheus.remote_write.mimir.receiver]
}

prometheus.remote_write "mimir" {
  url = "http://YOUR_SERVER/api/v1/push"
}

```

## Author

Oriol Rius

- email: <oriol@joor.net>

- https://oriolrius.me - Professional services

- https://oriolrius.cat - Personal blog since, July 2000

## License

This project is licensed under the MIT License.
