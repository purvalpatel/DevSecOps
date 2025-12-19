
Pre-commit time and Thread modeling tools:
-----------------------------------------
## Git-secrets:

git-secrets :   AWS labs tool preventing you from commiting secrets to a git repository. <br>

### install git-secrets:
```
apt-get install git-secrets
```

### Initialize git-secrets in your repository

From inside your Git repo: <br>
```
cd your-repo
git secrets --install
```

### block tokens/passwords
```
git secrets --add 'password\s*=\s*.+'
git secrets --add 'api[_-]?key\s*=\s*.+'
git secrets --add 'secret\s*=\s*.+'
git secrets --add 'token\s*=\s*.+'
```
Find secrets already commited:
```
git secrets --scan
```

Below is the project level setup script: `git-secrets-setup.sh`:
```
#!/bin/bash
git secrets --install
git secrets --register-aws
git secrets --add 'password\s*=\s*.+'
git secrets --add 'token\s*=\s*.+'
```
List configured patterns:
```
git config --get-all secrets.patterns
```

