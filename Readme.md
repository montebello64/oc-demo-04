
# oc-demo-04
oc new-project oc-demo-04  
oc project oc-demo-04

# Create service from a docker hub image
oc new-app montebello64/oc-demo-04-rest-name --name rest-name -e SPRING_PROFILES_ACTIVE=openshift -l microservice=oc-demo-04

oc new-app montebello64/oc-demo-04-rest-greeting --name rest-greeting -e SPRING_PROFILES_ACTIVE=openshift -l microservice=oc-demo-04

oc new-app montebello64/oc-demo-04-rest-consumer --name rest-consumer -e SPRING_PROFILES_ACTIVE=openshift -l microservice=oc-demo-04

# docker compose
docker-compose up --build

docker-compose down --volumes
