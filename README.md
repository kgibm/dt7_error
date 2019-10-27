# dt7_error
1. Build images:
```
docker build -t dt7_19009_javaee8  -f Dockerfile.19009.javaee8  .
docker build -t dt7_190010_javaee7 -f Dockerfile.190010.javaee7  .
docker build -t dt7_190010_javaee8 -f Dockerfile.190010.javaee8  .
```

2. Run Images
```
docker run -d -p 9080:9082 dt7_19009_javaee8
docker run -d -p 9081:9082 dt7_190010_javaee7
docker run -d -p 9082:9082 dt7_190010_javaee8
```

3. Login
```
localhost:9080/daytrader/welcome.faces - works
localhost:9081/daytrader/welcome.faces - works
localhost:9082/daytrader/welcome.faces - fails
```
