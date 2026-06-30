# OWSAP-ZAP
- ZAP Attack proxy is one of the most popular open-source web application security testing tools.
- Think of it as a proxy that sits between your browser and  the website, inspecting and testing requests and responses for vulnerabilities.

[download link](https://release-assets.githubusercontent.com/github-production-release-asset/36817565/d68f5516-26c1-4f2c-b51d-08c911dfbef8?sp=r&sv=2018-11-09&sr=b&spr=https&se=2026-06-30T05%3A56%3A19Z&rscd=attachment%3B+filename%3DZAP_2.17.0_Linux.tar.gz&rsct=application%2Foctet-stream&skoid=96c2d410-5711-43a1-aedd-ab1947aa7ab0&sktid=398a6654-997b-47e9-b12b-9515b896b4de&skt=2026-06-30T04%3A55%3A34Z&ske=2026-06-30T05%3A56%3A19Z&sks=b&skv=2018-11-09&sig=L4%2BA9l7OL%2BbEWPQMnVCRhzADKu4cZu2eOGK9qbNx4R0%3D&jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmVsZWFzZS1hc3NldHMuZ2l0aHVidXNlcmNvbnRlbnQuY29tIiwia2V5Ijoia2V5MSIsImV4cCI6MTc4Mjc5OTk4NiwibmJmIjoxNzgyNzk2Mzg2LCJwYXRoIjoicmVsZWFzZWFzc2V0cHJvZHVjdGlvbi5ibG9iLmNvcmUud2luZG93cy5uZXQifQ.MmYAL46zaUrZjvk0bzgSseYeoLkxpXvmfrgmWG4ZEF0&response-content-disposition=attachment%3B%20filename%3DZAP_2.17.0_Linux.tar.gz&response-content-type=application%2Foctet-stream)

Start Application:
```
## install java if not installed.
java -jar zap-2.17.0.jar
```
### Automated scan:
```
docker run --rm -t \
ghcr.io/zaproxy/zaproxy:stable \
zap-baseline.py \
-t https://yourwebsite.com
```
This performs:
- Spidering ( crawl pages )
- Passive vulnerability scanning
- Security header checks
- Generates findings

Safe for production environments because it doesnt actively attack the application.
