# rubin-rucio-deploy

Deployment scripts for Rubin USDF Rucio. Work in progress.

Once you have a access to your k8s cluster, you can deploy this with

    make apply

in the back, this uses `kustomize` to allow modification of helm template outputs from the official rucio helm chart. we probably want to lock to specific versions of the helm chart for produciton purpoases.
uses zalanda postgres operator to help manage the database.

to update, one should run

    make helm  # update from upstream helm charts
    make apply

still to do:
- connect rucio to the postgres database
- certs and other stuff
- general does this even work...

