# Face Pose Estimation with OpenCV & Dlib

 Jupyter notebook showing how to estimate face pose detection (which way someone is looking) and categorises it - currently just as looking left, centre or right, and up, level and down.



## Installation of dependencies on OSX

Getting everything to work can be a pain - this is what worked for me

```bash
# make sure you have brew
$ which brew
# if no path is returned install it with
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

# make sure you have pip
$ which pip
# if no path is returned install it with
$ sudo easy_install pip

# check if you have opencv for python
$ python3 -c "import cv2"
# if an error is returned
$ brew install opencv
# same error as above will still be returned but we’ll get back to that later

# check if you have dlib for python
$ python3 -c "import dlib"
# if an error is returned, run the following 
$ brew install boost-python
# double check if that worked
$ brew list | grep 'boost'
# this should return:
# boost
# boost-python

# make sure you have cmake
$ which cmake
# if no path is returned:
$ brew install cmake

# okay we are far!

# use the cd command to get into the directory that you downloaded this repo to
# then make a new virtualenv
$ python3 -m venv env
# and activate it
$ source env/bin/activate
# now we install opencv-python
$ pip3 install opencv-python
# now we install numpy and scipy
$ pip3 install numpy scipy
# opencv will now work

# now we install dlib
$ pip3 install dlib

# puuuh this is a lot but these should now not though errors anymore:
$ python3 -c "import cv2"
$ python3 -c "import dlib”
```

## Usage

Download the file you find at [https://github.com/biometrics/openbr-models/blob/master/dlib/shape_predictor_68_face_landmarks.dat](https://github.com/biometrics/openbr-models/blob/master/dlib/shape_predictor_68_face_landmarks.dat) and just put it into the root of your project folder.

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)