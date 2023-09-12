# GitHub Action: Update Deployment Manifest
This GitHub Action is designed to update a deployment manifest by replacing the old image tag with the a new one. It helps automate the process of keeping a deployment configuration up-to-date with the latest image reference, making it easier to manage applications deployed with ArgoCD.

## Security Note
Ensure that the G_TOKEN secret is securely stored in the repository's GitHub Secrets to grant the action access to the deployment repository.
