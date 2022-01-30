# myamplifyproject

ここでやれます

https://aws.amazon.com/jp/blogs/startup/event-report-amplify-handson/



```docker-compose.yml
version: '3.8'
services:
  ap:
    build:
      context: .
      dockerfile: Dockerfile
    container_name: ap
    ports:
      - "8080:8080"
    volumes:
      - ${PWD}/container:/container
    #command: rails s -b 0.0.0.0
    #command: /bin/bash
    tty: true
```

```Dockerfile
# Debian(v11) 
FROM amazonlinux:2

# パッケージアップデート
RUN yum -y update && yum -y upgrade
RUN yum -y install \
    git
    
RUN curl -sL https://rpm.nodesource.com/setup_16.x | bash -
RUN yum -y install nodejs

CMD ["/bin/bash"]
```


## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
