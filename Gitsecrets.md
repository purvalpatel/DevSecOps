```
docker run --rm   -v "$(pwd)/Sample-mlops-project:/repo"   -w /repo   zricethezav/gitleaks:latest   detect --source /repo --verbose
```
