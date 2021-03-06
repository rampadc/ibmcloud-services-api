Get a list of IBM Cloud services.

- `/`: all services offered
- `/ibm`: all services offered by IBM

Required environment variables:

```bash
export GLOBAL_CATALOG_URL=https://globalcatalog.cloud.ibm.com/api/v1
export GLOBAL_CATALOG_AUTHTYPE=iam
export GLOBAL_CATALOG_APIKEY=<API_KEY>
```

Local dev env with: `uvicorn app.main:app --reload`

Built image: `quay.io/congxdev/ibmcloud-services-api:latest`.

Build (replace image location with your image repository and update the tag accordingly):

```sh
podman build . -t quay.io/congxdev/ibmcloud-services-api:0.0.4
podman push quay.io/congxdev/ibmcloud-services-api:0.0.4
```