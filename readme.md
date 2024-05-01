# Deploy an app to GCP using Cloud Build

A basic example to deploy a "Hello, world" Flask app to a GKE cluster.

Requires:
- a GCP project with billing activated
- a GKE cluster (tested with a 3-node standard GKE cluster) with separate namespaces for production (main) and development branches
- GCP artifact repositories for production (main) and development branches
- Cloud Build triggers connected to this repository using cloudbuild.yaml for both branches

Uses
- a minimal Flask app: app.py
- requirements.txt to install flask
- Dockerfile to define the container image
- cloudbuild.yaml to build the container image and push it to the GCP artifact repository
- gke.yaml to deploy the app and expose the service

