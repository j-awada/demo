# A demo repo to demo things

### Act

```Bash
# Install on Mac
brew install act
act --version

# Run workflow locally
act workflow_dispatch -W .github/workflows/local.yaml

# OR if you are having issues with the Docker image locally
docker pull catthehacker/ubuntu:act-latest
act workflow_dispatch -W .github/workflows/local.yaml --container-architecture linux/arm64 --pull=false
```

**Using secrets:**

```Bash
touch .secrets
echo ".secrets" >> .gitignore
act workflow_dispatch -W .github/workflows/local.yaml --secret-file .secrets
```
