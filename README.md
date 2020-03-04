# demo-frontend

## odo

Deploy backend first <https://github.com/kadel/demo-backend> !

```bash
git clone  https://github.com/kadel/demo-frontend
cd frontend

odo create nodejs frontend --port 3000
odo url create
odo push
odo link backend
# access your application in url shown in `odo push` output
```

## Notes

Dockerfile - <https://gist.github.com/kadel/3a66a3b178fdddab4e4c72b2a9498975>  
