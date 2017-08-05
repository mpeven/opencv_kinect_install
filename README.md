## Warning

This is not tested on many systems. __YMMV__


## Requirements

- Have virtualenv and virtualenvwrapper set up (use virtualenvwrapper plugin for oh-my-zsh to make this easy)


## How to run

No gpu:
```
source opencv_install
```

gpu:
```
source opencv_install_cuda
```


## How to use

When making a new virtual environment:
```
mkvirtualenv <venv name> -p python3.6
pip install numpy
cp ~/.virtualenvs/opencv_install/lib/python3.6/site-packages/cv2*.so ~/.virtualenvs/<venv name>/lib/python3.6/site-packages
```
- Can now `import cv2` in a python script


## Testing

```
python /opt/src/opencv33_py36/samples/python/video.py
```



## Uninstalling

```
rm -rf /opt/src
rm -rf /opt/opencv33_py36
```
