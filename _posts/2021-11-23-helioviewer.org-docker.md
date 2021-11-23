---
title: Running HelioViewer in a Docker Container
date: 2021-11-23T14:30:00-00:00
author: Daniel Garcia Briseno
layout: post
permalink: /2021/11/23/helioviewer.org-docker/
categories:
  - General
---

HelioViewer can run in a container!

The container works by mounting the API, Site, and Sample data into
the container which runs both MySQL and an Apache Webserver. With
the container running locally, you can easily view and test changes
on HelioViewer.

If you would like to set up your own HelioViewer container, follow
the instructions below. If you would like to contribute to the container
you can make a pull request on [github](https://github.com/Helioviewer-Project/helioviewer.org-docker)

## Requirements
For this setup, you will need:
- [Docker Desktop](https://docs.docker.com/get-docker/)
- [Git](https://git-scm.com/)
- [Sample Data](http://helioviewer.org/jp2/archives/sample-data.tgz)

## Steps
1. First clone helioviewer.org and the API
```bash
git clone https://github.com/Helioviewer-Project/helioviewer.org.git
git clone https://github.com/Helioviewer-Project/api
```

2. Extract the sample data to a folder. Your directory structure should look like this:
```
- api
- helioviewer.org
- sample-data
| - AIA
| - HMI
```

3. Pull the docker container
```bash
docker pull dgarciabriseno/helioviewer.org-docker:latest
```

4. Run the container while specifying the volumes to each folder:
```
docker run \
    -p 127.0.0.1:8080:80 \
    -p 127.0.0.1:8081:81 \
    -v "$PWD/api:/var/www-api/api.helioviewer.org" \
    -v "$PWD/helioviewer.org:/var/www-api/docroot" \
    -v "$PWD/sample-data:/var/www-api/jp2" \
    -d \
    -t dgarciabriseno/helioviewer.org-docker:latest
```

5. Once the container starts, open up a shell in it and run the install script
```
./install.sh
```
At the prompts, enter the following:
![Prompt](/images/uploads/2021/install_prompt.png)

6. All done! Open your local helioviewer at [http://localhost:8080](http://localhost:8080)