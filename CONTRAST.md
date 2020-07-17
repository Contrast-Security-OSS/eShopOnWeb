
# This README is intended to provide the basic instructions on configuring the Contrast DOTNET CORE agent in eShopOnWeb

## Modifications made to the source project
- DockerFile updated to install Contrast's .NET Core agent
```dotnet add package Contrast.SensorsNetCore --version 1.5.11```
- docker-compose.yml updates to configure Contrast .NET Core agent's

## Steps

1. Configure Contrast connection environmental variables
Edit the docker-compose.yml file and update the following API authentication parameters.  
NOTE: If you are unsure of the values please visit our main documentation on this here: https://docs.contrastsecurity.com/en/find-the-agent-keys.html

Authentication:
```
      - CONTRAST__API__URL=https://app.contrastsecurity.com/Contrast
      - CONTRAST__API__API_KEY={agent API KEY}
      - CONTRAST__API__SERVICE_KEY={agent Service key}
      - CONTRAST__API__USER_NAME={agent user name}
```
2. Refer to the /README.md's "Running the sample using Docker" section to build and deploy the container.