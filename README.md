# A demo repo to demo things

### Act

```Bash
# Install on Mac
brew install act
act --version

# Run workflow locally
act workflow_dispatch -W .github/workflows/local.yaml
```

**Using secrets:**

```Bash
touch .secrets
echo ".secrets" >> .gitignore
act workflow_dispatch -W .github/workflows/local.yaml --secret-file .secrets
```
