---
layout: page
title: Installing Helioviewer
permalink: /install/
---

## To Use

Simply visit [Helioviewer.org](https://helioviewer.org)

However, if you wish to install the Helioviewer Project on your own machine this document has been created to aid you in this process.

## Run With Docker
This is the preferred way to run Helioviewer on your system.
Note that this container is designed as a development environment and should not be used for a production mirror.
This requires that you have both docker and git installed.

In a terminal, run the following commands to perform a clean install.
```bash
mkdir helioviewer-docker
cd helioviewer-docker
git clone https://github.com/helioviewer-Project/api
git clone https://github.com/helioviewer-Project/helioviewer.org
cd helioviewer.org
git submodule update --init --recursive
cd ..
docker run -p 127.0.0.1:8080:80 -p 127.0.0.1:8081:81 -v "$PWD/api:/home/helioviewer/api.helioviewer.org" -v "$PWD/helioviewer.org:/home/helioviewer/helioviewer.org" -d -t dgarciabriseno/helioviewer.org
```
This will do the following:
1. Create a folder called helioviewer-docker in the directory that you run the above commands
2. This will download the source code for Helioviewer's [API](https://github.com/Helioviewer-Project/api) and [Webserver](https://github.com/Helioviewer-Project/helioviewer.org)
3. Run the docker container which hosts the webserver and back end processes needed to run host helioviewer.

Wait for the container to initialize.
When looking at the logs, wait until you see the message "Container up and running."
You can now view helioviewer at [localhost:8000](http://localhost:8000)

The container takes care of all the **Manual Installation** steps seen below.

## Manual Installation
This is typically not recommended, but may be the preferred installation method if you need more control over what's running on your server, for example if you plan on hosting a Helioviewer mirror.

Specific distro instructions are not listed here.
Helioviewer will run on any linux distro as long as the dependencies are met.

### Dependencices
- >= PHP 8.0
- Following PHP modules: mysqli redis imagick bcmath mbstring curl openssl sockets.
(Some of these are php defaults, others need to be installed via package manager.)
- Redis & php-redis (`pecl install redis`)
- Image Magick >= 6.9.12 & php-imagick (`pecl install imagick`)
- MySQL
- >= Python 3.8 (lower versions of Python 3 may be ok)
- Following python libraries: numpy sunpy matplotlib scipy glymur mysqlclient
- tcsh
- Apache Ant
- Web server that runs PHP (nginx/apache/etc)
- Ruby & the Resque gem
- ffmpeg

### Clone source-code

Clone the api repository into webroot usually located in “/var/www”

`git clone https://github.com/Helioviewer-Project/api.git api.helioviewer.org`

Clone the front-end repository into webroot usually located in “/var/www”

`git clone https://github.com/Helioviewer-Project/helioviewer.org.git`

cd into the helioviewer.org folder and run the following command to pull in
project dependencies

`git submodule update --init`

###  Setup Kakadu

Kakadu binaries and shared libraries for 32-bit and 64-bit linux can be found in the install/kakadu directory. Select the appropriate archive based on your architecture and extract the files:

`cd install/kakadu`

`tar zxvpf Kakadu_v6_4_1-00781N_Linux-64-bit-Compiled.tar.gz`

Next, copy the Kakadu shared libraries and binaries to a known path, e.g.:

`sudo cp lib/* /usr/local/lib/`

`sudo cp bin/* /usr/local/bin`

Update dynamic linker cache:

`sudo -s # enter root shell`

`ldconfig`

`exit # exit root shell`

Now try running one of the Kakadu tools to make sure everything was set up properly:

`kdu_merge`

### Setup the Database

The next step is to process your JPEG 2000 (JP2) images and enter their information into the database for efficient querying.
If you don't already have a JP2 dataset, you can download a sample dataset, e.g.:

`wget http://helioviewer.org/jp2/archives/sample-data.tgz`

`mkdir /var/www/jp2/`

`tar zxvpf sample-data.tgz -C /var/www/jp2`

If the MySQL daemon is not already running, start it:

`sudo service mysql start`

Change to the "api/install" directory and run the Helioviewer installation script:

`python3 install.py`

Follow the steps shown on screen. Processing the JPEG 2000 archive may take anywhere from several minutes to many hours depending on the size of the archives, and the number of files to be processed. For a small dataset like the sample one provided above, processing should only be a matter of minutes.

### Create Caching/Logging Directories

In order to function properly, Helioviewer requires write-access to several directories. Tiles, screenshots, and movies are stored in a "cache" directory and logs are stored in a "log" directory. Additionally, if you plan to use a JPIP server in conjunction with Helioviewer, a "movies" directory must be created within the JPEG 2000 archive so that generated JPX files may be accessed over JPIP.

`mkdir -p log cache jp2/movies`

Enable Apache to write to the directories:

`chgrp www-data log cache jp2/movies`

`chmod 755 log cache jp2/movies`

### Modify Config File

Both the front-end and back-end of Helioviewer.org use a single configuration file named "Config.ini", in addition to a separate database configuration file, "Private.php." Both of these files are located in the api/settings directory. Example files, "Config.Example.ini" and "Private.Example.php," are provided which are intended to be used as a basis for your own configuration.

Copy or rename these example files to "api/settings/Config.ini" and "api/settings/Private.php", respectively.

Modify the "Config.ini" file so that the information (filepaths, etc) accurately reflect your server configuration.

By default, the "compress_js" and "compress_css" parameters are set to "true" and Helioviewer will expect to find minified versions of the javascript code and cascading stylesheets. Either set these parameters to "false", or run Apache Ant on the "scripts/build.xml" file to build the necessary products:

`cd helioviewer/resources/build`

`ant`

Modify the database credentials in the "Private.php" file with the values you entered in the installation GUI.

It is recommended to use a virtual host configuration within apache to direct requets to the api under a subdomain.

All done!


To test the installation, open your web browser of choice and navigate to the location where Helioviewer is installed. If you installed Helioviewer to /var/www/helioviewer, you can view the website at http://localhost/helioviewer/.
