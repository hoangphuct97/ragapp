
## README

### Deploying the Application on Docker using Docker Swarm

To deploy the application on Docker using Docker Swarm, follow these steps:

1. **Initialize Docker Swarm (if not already initialized)**:
   ```sh
   docker swarm init
   ```

2. **Deploy the Application**:
   Run the following command to deploy the application using Docker Swarm:
   ```sh
   MODEL=llama3 docker stack deploy -c docker-compose.yml ragapp_stack
   ```

### Removing the Deployed Application

If you need to remove the currently deployed application, use the following command:
```sh
docker stack rm ragapp_stack
```

### Additional Information

- Ensure Docker and Docker Swarm are properly installed and configured on your machine.
- The `docker-compose.yml` file should be present in the directory where you run these commands.
- The `MODEL=llama3` environment variable sets the model version used in the deployment.

For more detailed information, refer to the official Docker documentation: [Docker Documentation](https://docs.docker.com/).

### Troubleshooting

- **Swarm not initialized**: If you encounter errors related to Docker Swarm not being initialized, make sure to run `docker swarm init`.
- **File not found**: Ensure that the `docker-compose.yml` file exists in the current directory.

If you face any other issues, please check the logs or refer to the Docker documentation for troubleshooting tips.

---

This README file provides the basic commands to deploy and remove the application using Docker Swarm. For further customization and configuration, you may need to modify the `docker-compose.yml` file accordingly.
