# python-alpine


[![dockeri.co](http://dockeri.co/image/drivetech/python-alpine)](https://hub.docker.com/r/drivetech/python-alpine/)

[![Build Status](https://travis-ci.org/Drivetech/python-alpine.svg?branch=master)](https://travis-ci.org/Drivetech/python-alpine)

> Docker Image for python/django apps with alpine linux and dependencies for postgresql, pillow, lxml and fii

- 3.6.2, 3.6, 3, latest ([3.6/Dockerfile](https://github.com/Drivetech/python-alpine/blob/master/3.6.2/Dockerfile))
- 3.6.2-onbuild, 3.6-onbuild, 3-onbuild, onbuild ([3.6/onbuild/Dockerfile](https://github.com/Drivetech/python-alpine/blob/master/3.6.2/onbuild/Dockerfile))
- 3.6.2-flake8, 3.6-flake8, 3-flake8, flake8 ([3.6/flake8/Dockerfile](https://github.com/Drivetech/python-alpine/blob/master/3.6.2/flake8/Dockerfile))
- 2.7.13, 2.7, 2 ([2.7/Dockerfile](https://github.com/Drivetech/python-alpine/blob/master/2.7.13/Dockerfile))
- 2.7.13-onbuild, 2.7-onbuild, 2-onbuild ([2.7/onbuild/Dockerfile](https://github.com/Drivetech/python-alpine/blob/master/2.7.13/onbuild/Dockerfile))
- 2.7.13-flake8, 2.7-flake8, 2-flake8 ([2.7/flake8/Dockerfile](https://github.com/Drivetech/python-alpine/blob/master/2.7.13/flake8/Dockerfile))

## Create a Dockerfile in your Python app project
```dockerfile
FROM drivetech/python-alpine:3-onbuild
# replace this with your application's default port
EXPOSE 8000
CMD [ "python", "app.py" ]
```

You can then build and run the Docker image:

```bash
docker build -t my-python-app .
docker run -it --rm --name my-running-app my-python-app
```

### Notes
The image assumes that your application has a file named package.json listing its dependencies and defining its start script.
