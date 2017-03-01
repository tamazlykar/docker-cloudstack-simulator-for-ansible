# CloudStack Simulator as Docker Image

The purpose of this docker image is to run automated integration tests for the CloudStack modules in Ansible.

## Setup

The docker image runs the CloudStack simulator and contains two zones for the different network setups: `basic` and `advanced` networking.

* CloudStack Zone: Sandbox-simulator-advanced
* Zone: Sandbox-simulator-basic

## Build

    docker build -t cloudstack/simulator .

## Run

    docker run --name cloudstack -d -p 8888:8888 cloudstack/simulator

NOTE: It may take some time until the zones are deployed. The web server will respond with HTTP 503 on port 8888 unless the zones are fully deployed.
