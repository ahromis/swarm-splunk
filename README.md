# swarm-splunk

A set of Docker Compose files to run Splunk using Docker Swarm.

## Usage

1. Clone this repo
2. `SPLUNK_NODE=<node_to_deploy_splunk_on> docker stack deploy -c ./splunk/docker-compose.yml splunk`
3. `docker stack deploy -c ./splunk/docker-compose.yml splunk-forwarder`

If you just need to run the forwarder and have Splunk already running outside of your swarm cluster, then edit the compose file for the forwarder where `SPLUNK_FORWARD_SERVER: splunk:9997` would point to your existing Splunk installation.
