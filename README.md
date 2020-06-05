# ITCS381_Assignment2-3_2020
ITCS381_A2-3r_#2[Color]_6188053_6188058_6188071

## Installation

Open Anaconda Prompt(Anaconda3) and use the package manager [pip](https://pip.pypa.io/en/stable/) to install.

for windows if you have anaconda installed, you can simply do
```bash
pip install opencv-python
```
or
```bash
conda install -c https://conda.binstar.org/menpo opencv
```

## Usage
You can run the file named "ITCS381_A2-3JupyterNB_#2[Color]_6188053_6188058_6188071.ipynb" on The Jupyter Notebook(Anaconda3) 
to test and see the result on it.

If you doesn't have Jupyter Notebook you can see the Python code in file named "ITCS381_A2-3Pycode_#2[Color]_6188053_6188058_6188071"

You have to put 2 images in the same folder of Jupyter file to run the program , if you want to change the image, you can do by change
the name of Image1 or Image2 in the code.

```python
import cv2
import numpy as np
from matplotlib import pyplot as plt

Image1 = 'Pinterest_FishTatoo.png' #Change file name Here.
Image2 = 'Piero.png'

img = cv2.imread(Image1)
color = ('b','g','r')
plt.figure()
plt.title("Color Histogram")
for i,col in enumerate(color):
    histr = cv2.calcHist([img],[i],None,[256],[0,256])
    plt.plot(histr,color = col)
    plt.xlim([0,256])
plt.show()
```


