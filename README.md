# Philippine Textiles Classification

This project focuses on the recognition of Philippines indigenous textile patterns using Convolutional Neural Networks (CNN). The goal is to develop a system that can automatically identify and classify various traditional textile patterns found in the Philippines, utilizing TensorFlow and MobileNetV2.

![Sample Output](captured_images/binetwagan/2022-01-01-17-03-45.jpg)

## Languages and Tools Used

The project was developed using the following languages and tools:

- Python 3
- TensorFlow
- OpenCV
- Qt5

## Setup

### Windows

- Python 3.8 above and pip must be installed in your computer.
- Clone this repository, open the terminal, change directory to the cloned repository and follow the commands below.
- Install virtualenv package: `pip install virtualenv`
- Install Qt5 or QtDesigner (optional) if you want to edit the GUI.
- Create a virtual environment. Lets name it my-venv: `virtualenv my-venv`
- Activate virtual environment: `my-venv/Scripts/activate`
- Install the required packages: `pip install -r requirements.txt`
- Run the main program: `python main.py`

### Raspberry Pi/Linux

The required Python modules are listed in the requirements.txt file. However, when using Raspberry Pi, it is necessary to manually install some modules due to version compatibility issues. Follow the steps below:

#### Update and upgrade the system:

```
sudo apt update
sudo apt upgrade
reboot
```

#### Install TensorFlow for ARM architecture:

```
pip3 install https://github.com/bitsy-ai/tensorflow-arm-bin/releases/download/v2.4.0/tensorflow-2.4.0-cp37-none-linux_armv7l.whl --no-cache-dir
```

#### Install additional required modules:

```
pip3 install tensorflow_hub
pip3 install opencv-python
pip3 install matplotlib
pip3 install numpy=="1.19.5"
pip3 install seaborn
pip3 install pyyaml h5py
sudo apt-get install python3-pyqt5
sudo apt-get install libatlas-base-dev
sudo apt-get install libjasper-dev
sudo apt-get install libqtgui4
sudo apt install libqt4-test
reboot
```

#### Enable Raspberry Pi Camera module:

```
sudo modprobe bcm2835-v4l2
```

Then use the command `sudo raspi-config` to enable it.

Reboot and run the main program again: `python main.py`

In the older version of Raspbian, `python` still points to Python 2. If the command above doesn't work, use `python3 main.py`.
