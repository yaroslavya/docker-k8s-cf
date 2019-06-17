Dockerize angular app
=====================

1. add a Dockerfile to the root folder. make the needed build steps, they can be made one by one
without actually building the app.

2. add .dockerignore file to the root folder. make sure node_modules and .git folders are ignored.

3. start the build by `docker build -t test-app -f Dockerfile .`

4. once the container is built run it by `docker run --rm --name test-dev -p 8080:80 test-app`

5. the app should be accessible at http://localhost:8080/

this can be an issue: [https://github.com/npm/npm/issues/16661](https://github.com/npm/npm/issues/16661)

