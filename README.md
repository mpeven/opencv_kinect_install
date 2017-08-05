## Warning

This is not tested on many systems. __YMMV__


## Requirements

- Have virtualenv and virtualenvwrapper set up (use virtualenvwrapper plugin for oh-my-zsh to make this easy)


## How to run

No gpu:
```
source opencv_install
source freenect_python_install
```

gpu:
```
source opencv_install_cuda
source freenect_python_install
```


## How to use

When making a new virtual environment:
```
mkvirtualenv <venv name> -p python3.6
pip install numpy
cp /opt/src/opencv33_py36/release/lib/python3/cv2.cpython-36m-x86_64-linux-gnu.so ~/.virtualenvs/<venv name>/lib/python3.6/site-packages
cp /opt/freenect_py36/lib/python3.6/site-packages/freenect.so ~.virtualenvs/<venv name>/lib/python3.6/site-packages/
```
- Can now `import cv2, freenect` in a python script


## Testing

```
python /opt/src/opencv33_py36/samples/python/video.py
```



## Uninstalling

```
rm -rf /opt/src
rm -rf /opt/opencv33_py36
rm -rf /opt/freenect_py36
```
