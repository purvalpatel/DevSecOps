# sqlmap
 - Scan for SQL injection
Reference : https://github.com/sqlmapproject/sqlmap/wiki/Screenshots

### How to download:
```
git clone --depth 1 https://github.com/sqlmapproject/sqlmap.git sqlmap-dev

cd sqlmap-dev
python3 sqlmap.py -h
```
### How to test:
```
python3 sqlmap.py -u "https://flitrack.com/jsp/flitrack_login.jsp?id=1" --batch
```
