# BenJail instagram Sample #

![BenJail instagram Sample Version](https://img.shields.io/badge/Version-0.0.4-green.svg)

## Summary

This sample contains a Django 2.0.x Instagram Site. The  images are optimized for performance. The Django instagram Sample is responsive and mobile/device friendly.

![Django instagram Sample](./staticfiles/home.png)

### Create a profile from the Django admin panel

Albums can be created from the Django admin panel where one zip file with all the images should be selected from the PC. The Django instagram will resize the images to improve the picute load times and will also create thumbnail for every image in the zip.

![Django instagram Sample](./staticfiles/admin.png)


## Tested with Django / Python
![Python](https://img.shields.io/badge/Python-3.6-green.svg)
![Django](https://img.shields.io/badge/Django-2.2.3-green.svg)

## Additional Django apps dependencies
- Pillow
- django-imagekit

## Additional JavaScript apps dependencies
- jquery
- photoswipe

## Prerequisites

- Django-Python [development environment](#) already set up.
- virtualenv installed.

## Solution

Solution|Author(s)
--------|---------
BenJail instagram | Benson owino ([@benson](https://twitter.com/Ben58886580))

## Version history

Version|Date|Comments
-------|----|--------
0.0.1|feb 27, 2020 | Updated to Django 2.2.3

## Disclaimer
**THIS CODE IS PROVIDED *AS IS* WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESS OR IMPLIED, INCLUDING ANY IMPLIED WARRANTIES OF FITNESS FOR A PARTICULAR PURPOSE, MERCHANTABILITY, OR NON-INFRINGEMENT.**

---

## Minimal Path to Awesome

- Clone this repository.
- Open the command line, navigate to the django app folder and execute:
    - `virtualenv env` (requires virtualenv), Mac `virtualenv yourenv -p python3.6`
    - Linux: `source env/bin/activate`, Windows: `call env/Scripts/activate.bat`, Mac `source env/bin/activate`
    - navigate to the `django_instagram` folder using `cd django_instagram`
    - execute `pip install -r requirements.txt` or `pip3 install -r requirements.txt` depending on your python installation. 
    - If the Pillow fail to install on Windows, then install it manually `pip install ../whl/Pillow-5.0.0-cp36-none-win32.whl` (if you are not using python 3.6 32 bit then  [download the Pillow wheel](http://www.lfd.uci.edu/~gohlke/pythonlibs/#pillow) for your python version).
    - Run `python manage.py migrate` or `python3 manage.py migrate`
    - Run `python manage.py runserver` or `python3 manage.py runserver` depending on your python installation
    - Open http://127.0.0.1:8000/ in web browser.
    - To access the admin forms go to http://127.0.0.1:8000/admin/ and enter user: benowino7, password: benjil100

## Features

This Sample illustrates the following concepts on top of the Django Framework:

- Using django-material and materializecss for building Django UI.
- Using django-imagekit for building resizing images.
- Using photoswipe javascript library for more rich instagram user experience.

## Control the image size and quality
The picture size and quality can be controlled programatically from the models.py. Just change the processors. For more information see [django-imagekit](https://github.com/benowino7/instaclone).

```python
class AlbumImage(models.Model):
    image = ProcessedImageField(upload_to='albums', processors=[ResizeToFit(1280)], format='JPEG', options={'quality': 70})
    thumb = ProcessedImageField(upload_to='albums', processors=[ResizeToFit(300)], format='JPEG', options={'quality': 80})
    ...
```

## Sample data cleanup
To cleanup the sample data delete the sql lite database and the media folder files. Create new database and run the sample again.

## No validation on the form
This is sample. I decided to keep it simple and let the validation to be added.

## Sharing is Caring

Star if you like it :)
