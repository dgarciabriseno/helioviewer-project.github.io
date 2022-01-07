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

(Edited: 01/07/2022)

## Requirements
For this setup, you will need:
- [Docker Desktop](https://docs.docker.com/get-docker/)
- [Git](https://git-scm.com/)

## Steps
1. First clone helioviewer.org and the API
```bash
git clone https://github.com/Helioviewer-Project/helioviewer.org.git
git clone https://github.com/Helioviewer-Project/api.git
```

2. Extract the sample data to a folder. Your directory structure should look like this:
```
- api
- helioviewer.org
```

3. Pull the docker container
```bash
docker pull dgarciabriseno/helioviewer.org-docker:v1.3_setup_done
```

4. Run the container while specifying the volumes to each folder. The sample-data
   folder does not need to exist, it will be created when the command runs.
```
docker run \
    -p 127.0.0.1:8080:80 \
    -p 127.0.0.1:8081:81 \
    -v "$PWD/api:/var/www/api.helioviewer.org" \
    -v "$PWD/helioviewer.org:/var/www/docroot" \
    -v "$PWD/sample-data:/var/www/jp2" \
    -d \
    -t dgarciabriseno/helioviewer.org-docker:v1.3_setup_done
```

5. Once the container starts, view the log in docker and verify there are no errors. Please
   report any issues on our [github](https://github.com/Helioviewer-Project/helioviewer.org-docker)

6. Open your local helioviewer at [http://localhost:8080](http://localhost:8080)
   You should see the helioviewer GUI, but no images of the sun yet.

7. Inside the container's shell, execute the downloader script to begin downloading images to view.
```
# Easy setup script
bash ~/setup_files/scripts/download_data.sh
# Advanced install script
python3 /var/www/api.helioviewer.org/install/downloader.py -d lmsal -s "2022-01-01 00:00:00" -e "2022-01-02 00:00:00"
```
