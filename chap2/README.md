# How to build an image and shore it in an artifact repository
Create a new Docker repository named quickstart-docker-repo in the location us-west2 with the description "Docker repository":

```
gcloud artifacts repositories create quickstart-docker-repo --repository-format=docker --location=europe-west1 --description="Docker repository"
```

Verification: 
```
gcloud artifacts repositories list
```

Start the build with the following command: 
```
gcloud builds submit --region=europe-west1 --config  create_image.yaml
```

# Deploy a containerized application to Cloud Run using Cloud Build
Deploy on cloud run: 
```
gcloud builds submit --region=europe-west1 --config deploy_container.yaml
```