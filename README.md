# Coursera Offline

Download and save the video lectures of your favorite courses for offline viewing.

## Full Usage
```
usage: coursera_offline.py [-h] [-s SHORTNAME] [-e EMAIL] [-p PASSWORD] [-S]
                           [-f]

optional arguments:
  -h, --help            show this help message and exit
  -s SHORTNAME, --shortname SHORTNAME
                        Short name of the course being downloaded. This option
                        is required when running the script for the first time
  -e EMAIL, --email EMAIL
                        Email id registered with Coursera
  -p PASSWORD, --password PASSWORD
                        Coursera Password
  -S, --synch           Give this option to fetch the updated video content
  -f, --file            Give this option to forces the script to obtain the
                        course information from data.json instead of Coursera
```

## Some sample invocations

*Note:* In order to download some courses, you need to be registered for them in Coursera site before running the script.

#### First time download

```
coursera_offline -s interactivepython-005 -e <email> -p <password>
```

Do this to download the video lectures arranged as per weeks.This also creates a `data.json` file that contains all the information requried to download the videos.

#### Synching

```
coursera_offline -S -e <email> -p <password>
```

Okay, so you've been a few weeks into the course, now u need to fetch the updated videos. Don't worry there's a way to do it !
The above command takes care of fetching the updated video content and synching it with your local directories.

#### Fetch using file

```
coursera_offline -f -e <email> -p <password>
```
So, you might be wondering the point of saving the `data.json`, right ? That wasn't totally pointless either. The file's data is acquired by fetching the coursera video lectures page, parsing the html content. All the information required to download that course's videos is in that file. So, as long as you have the file, you can download the course without fetching the lecture page and the above command is the way to do it.

## Installation

* Make sure you have python version 2.7 installed. If you don't have python, get it from [here](https://www.python.org/download/releases/2.7/)
* If you have python and are not sure of the version, type `python -V` in the terminal. If it says 2.7.x+ then you're okay. Otherwise, go to the link provided above.
* Install `pip` using `sudo apt-get install python-pip`. Install the application using `sudo pip install coursera_offline`
* If you don't want to install pip, you can download the tar.gz from [PyPi](https://pypi.python.org/packages/source/c/coursera_offline/coursera_offline-0.1.0.tar.gz) or [Github](https://github.com/sanketh95/coursera-offline/archive/master.zip), extract the archive file and follow the installation instructions in the README.txt file.