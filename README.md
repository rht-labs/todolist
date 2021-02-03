# todolist
API backend built in NodeJS using Express to add TODOs to a MongoDB.
Front end for Todolist exposed on port 8080.

## Build and Run
`npm run dev`

## Start the db 
This requires Docker installed.
`npm run mongodb`


`oc process -f .openshift-applier/templates/todolist-deploy.yml \
    -p NAME=todolist \
    -p APP_TAG=latest \
    -p NAMESPACE=<YOUR_NAME> \
    | oc create -f -`