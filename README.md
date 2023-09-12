# ArgoCD Manifest Update GitHub Action
This GitHub Action helps automate the process of updating a deployment manifest in your deployment repository with the latest image hash for your application. It helps simplify keeping your application's deployment configuration up-to-date with the latest image references.

## Inputs

### `deployment-repo` (Required)
The deployment repository holding the deployment manifests.

### `github-token` (Required)
The GitHub Token required to access the deployment repository. Needs read and write access to deployment repository.

### `deployment-repo-ref` (Optional)
The deployment repository ref to be used (default: 'main').

### `manifest-file` (Required)
The path of the manifest file in your deployment repository.

### `image-name` (Required)
The Docker image name.

### `image-tag` (Required)
The new tag value.

### `git-email` (Optional)
The email to be used for the Git commit (default: 'pujux@argocd-manifest-update.com').

### `git-name` (Optional)
The username to be used for the Git commit (default: 'pujux').

## Usage
To use the ArgoCD Manifest Update GitHub Action in your workflow, you can add the following YAML code to your repository's workflow file. Be sure to customize the values according to your project's needs.

```yaml
- name: ArgoCD Manifest Update
  uses: <repository>/<action-name>@<tag>
  with:
    deployment-repo: <your-deployment-repo>
    github-token: ${{ secrets.DEPLOYMENT_REPO_TOKEN }}
    deployment-repo-ref: <your-deployment-repo-ref>  # Optional (default: 'main')
    manifest-file: <path-to-manifest-file>
    image-name: <your-image-name>
    image-tag: <new-image-tag>
    git-email: <git-user-email>  # Optional
    git-name: <git-username>     # Optional
```

## License
This GitHub Action is provided under the MIT License.

## Support
For any questions or issues related to this GitHub Action, you can reach out to the author, Julian Pufler, at julian@pufler.dev.
