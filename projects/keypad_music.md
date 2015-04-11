
Some notes on USB stuff in Python (I didn't really get this working at all yet):

```
brew install libusb
pip install libusb1

pip install --pre pyusb
https://github.com/walac/pyusb/blob/master/docs/tutorial.rst
http://walac.github.io/pyusb/

sudo ipython
import usb.core
dev = usb.core.find()
```

http://stackoverflow.com/questions/21687867/reading-from-a-usb-keyboard-in-python-with-a-timeout

http://people.csail.mit.edu/hubert/pyaudio/
