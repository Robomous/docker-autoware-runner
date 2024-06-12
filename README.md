<img src="https://robomous.ai/images/layout/robomous-banner.svg" alt="robomous.ai" width=300 />

-----------------

# Docker Autoware Runner
Docker compose configuration to can run autoware locally by docker.

## Local environment setup for Docker

Rename the env-sample.txt to .env and set the values for the environment variables.

```bash
cp env-sample.txt .env
```

## Running the docker compose

To run the docker compose, it's necessary to have the docker and docker-compose installed. After that, run the following command to run the autoware container with bash.

```bash
docker-compose run autoware bash
```

This is necessary to run the autoware correctly, because if you try to run the autoware ROS node directly, it will not work.

Now, you can run the autoware by running the following command:

```bash
ros2 launch autoware_launch planning_simulator.launch.xml map_path:=/autoware_map/sample-map-planning vehicle_model:=sample_vehicle sensor_model:=sample_sensor_kit
```
