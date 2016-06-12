### How to run the pasrse server and parse dashboard on the local machine

enter folder "docker-compsose" and run:
```
APP_ID=myAppId MASTER_KEY=myMasterKey PARSE_DASHBOARD_ALLOW_INSECURE_HTTP=true docker-compose up -d

APP_ID=myAppId MASTER_KEY=myMasterKey PARSE_DASHBOARD_ALLOW_INSECURE_HTTP=true USER1=ymruan USER1_PASSWORD=ymruan123 SERVER_URL=http://my-cms-qa:1337/parse docker-compose up
```
