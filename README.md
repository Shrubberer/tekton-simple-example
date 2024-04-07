# tekton-simple-example
A simple hello example with trigger

change namespace from "python" to your namespace
then 
kubectl create -f example-trigger.yaml
kubectl create -f say-things-pipeline.yaml

the event listener creates a service, expose it with oc expose service servicename
get the route url with oc get routes

trigger it with 

 curl -X POST $ROUTEURL -H 'Content-Type: application/json' -d '{"after": "c5fcb8c44ae7640994e6e3e6316fa138571433c9", "repository": {"name": "test"}}'
