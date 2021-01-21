Check how much memory currently used by apps:

```
psql -U qradar -c "select id, name, status, task_status, image_repo, memory from installed_application union select NULL as 
id, '' as name, '' as status, '' as task_status, '' as image_repo, sum(memory) from installed_application ORDER BY id;"
```

Start/stop application from the API
https://www.ibm.com/support/pages/qradar-starting-and-stopping-application-api
