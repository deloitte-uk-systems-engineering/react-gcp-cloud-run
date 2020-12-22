# React GCP Cloud Run

A reference project to deploy a React app onto Google Cloud Platform Cloud Run

Inspired by [this](https://cloud.google.com/community/tutorials/deploy-react-nginx-cloud-run) GCP Community blog post

## Enable APIs

In GCP console, create a new project and enable the following APIs:

- Cloud Run API
- Google Container Registry API
- Cloud Build API

## Build and deploy to GCP

- Please ensure you have [Google Cloud SDK](https://cloud.google.com/sdk/docs/install) installed locally. Then, run the following commands:

```bash
gcloud builds submit --tag gcr.io/<your_gcp_project_id>/gcp-cloud-run-react # build the image and push to gcp image registry
gcloud beta run deploy --image gcr.io/<your_gcp_project_id>/gcp-cloud-run-react --platform managed # deploy to Cloud Run!
```

- Find the Service URL in terminal output

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License

[MIT](https://choosealicense.com/licenses/mit/)
