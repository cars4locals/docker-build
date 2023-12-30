# Action to build multiarch images

## Usage

Inside your github action, create this step
```yaml
    steps:
      
      - name: Using action to build multiarch image
        uses: cars4locals/docker-build@v4.2
        with:
            ecr-repository:        # AWS ECR repository identifier
            image-tag:             # Desired image tag
            context:               # (OPTIONAL) Build context (default - '.' )
            file:                  # Path to Dockerfile (default - './Dockerfile' )
            build-args:            # (OPTIONAL) Build arguments
            platforms:             # (OPTIONAL) Platforms list (default - 'linux/amd64,linux/arm64' )
            aws-access-key-id:     # AWS access key ID
            aws-secret-access-key: # AWS secret key
            aws-region:            # (OPTIONAL) AWS Region (default - 'us-west-2')
```
