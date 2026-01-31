Check Secrets.
```
docker run --rm   -v "$(pwd)/Sample-mlops-project:/repo"   -w /repo   zricethezav/gitleaks:latest   detect --source /repo --verbose
```

Fail build if secret found. (CI Friendly )
```
docker run --rm \
  -v "$(pwd):/repo" \
  -w /repo \
  zricethezav/gitleaks:latest \
  detect --source /repo --exit-code 1
```
