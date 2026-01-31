### Check Secrets.
```
docker run --rm   -v "$(pwd)/Sample-mlops-project:/repo"   -w /repo   zricethezav/gitleaks:latest   detect --source /repo --verbose
```

### Fail build if secret found. (CI Friendly )
```
docker run --rm \
  -v "$(pwd):/repo" \
  -w /repo \
  zricethezav/gitleaks:latest \
  detect --source /repo --exit-code 1
```
###  Use custom config (.gitleaks.toml)
Place `.gitleaks.toml` in repo root:
```
[allowlist]
paths = ["docs/", "examples/"]
```

Run with config:
```
docker run --rm \
  -v "$(pwd):/repo" \
  -v "$(pwd)/.gitleaks.toml:/gitleaks.toml" \
  zricethezav/gitleaks:latest \
  detect --source /repo --config /gitleaks.toml
```

### Save Report to file:
```
docker run --rm \
  -v "$(pwd):/repo" \
  -v "$(pwd)/gitleaks-report:/output" \
  zricethezav/gitleaks:latest \
  detect --source /repo --report-format json --report-path /output/report.json

```

### Gitlab CI:
```
gitleaks:
  image: zricethezav/gitleaks:latest
  stage: test
  script:
    - gitleaks detect --source . --exit-code 1

```
