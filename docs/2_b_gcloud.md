```

GCP_PROJECT="flowing-gasket-309204"
APP_NAME=dr
REGION="asia-south1"
MEMORY=1G
cd <directory/name>
cd models/
wget <https://model/file/model.pkl>
gcloud builds submit --tag gcr.io/$GCP_PROJECT/$APP_NAME


gcloud beta run deploy $APP_NAME --image gcr.io/$GCP_PROJECT/$APP_NAME --region $REGION --memory $MEMORY --allow-unauthenticated

```
