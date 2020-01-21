# docker-registry-and-ui

# To install a registry:2:
docker-compose up -d

# To install the registry-ui:  
docker run -d --net docker_default -p 8080:80 -e REGISTRY_URL=http://my-url:5000 -e DELETE_IMAGES=true -e REGISTRY_TITLE="My registry" --link registry --name registry-ui joxit/docker-registry-ui:static

# After a reboot, only you need is a 'docker start  registry-ui'
