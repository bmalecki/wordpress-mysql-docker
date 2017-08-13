# 1. How to run
```
docker-compose -f stack.yml up
```

# 2. How to backup wordpress database
```
docker-compose -f stack.yml exec db sh -c "/usr/bin/mysqldump -u root -pexample --databases wordpress" | tail -n +2 > ./db/init/init.sql
```


#### And rebuild you db images!
```
docker-compose -f stack.yml build db
```
