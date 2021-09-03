
# QR Code Generator and Reader

In this tutorial, I will be showing you how to generate a QR Code and read it with the help of Python.

First we need to install the necessary packages `qrcode` and `cv2`.

```bash
pip install qrcode
```

```bash
pip install opencv-python
```

Now we just need to import our packages in our file.

```python
import qrcode
import cv2
```

Now we will just take the input from user of what we need to convert into qrcode(it can be text, number or anything.)
And our package will convert it into QR Code

```python
path = input("Enter link to create QR Code : ")
img = qrcode.make(path)
imgName = input("Enter save file name : ")
img.save(imgName+'.jpg')
```

Now we will just read the QR Codes using another package named `cv2`.

We take the input from user about the path of the qrcode we need to decode and our package will do it for us.

```python
d = cv2.QRCodeDetector()
path = input("Enter path to QR Code: ")
val, _, _ = d.detectAndDecode(cv2.imread(path))
print(val)
```

Now we are good to go.

We have successfully built a QR Code Generator and Reader.

  
