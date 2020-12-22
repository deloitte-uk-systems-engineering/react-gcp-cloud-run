# React GCP Cloud Run

A reference project to deploy a React app onto Google Cloud Platform Cloud Run

## Enable APIs

In GCP console, create a new project and enable the following APIs:

- Cloud Run API
- Google Container Registry API
- Cloud Build API

## Build and deploy to GCP

```bash
gcloud builds submit --tag gcr.io/<your_gcp_project_id>/gcp-cloud-run-react # build the image and push to gcp image registry
gcloud  beta run deploy --image gcr.io/<your_gcp_project_id>/gcp-cloud-run-react --platform managed # deploys to Cloud Run!
```

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License

[MIT](https://choosealicense.com/licenses/mit/)
