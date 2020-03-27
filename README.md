# Face Detection using OpenCV
Here we use haarcascade for detecting the faces which is trained by set of input data. 
Open cv contain cascade functions/classifiers for eyes,face etc.
# Requirement
Install Open cv
```python
pip install opencv-python
```
```python
import cv2
```

# Load the cascade
haarcascade face classifier is use which is 
```python
face_cascade = cv2.CascadeClassifier('haarcascade_frontalface_default.xml')
```
# Convert into grayscale
```python
gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)

```
# Detect faces
```python
faces = face_cascade.detectMultiScale(gray, 1.2, 4)
```
# Draw rectangle around the faces
```python
for (x, y, w, h) in faces:
    cv2.rectangle(img, (x, y), (x + w, y + h), (255, 0, 0), 2)
```
# for video
To capture video from webcam. 
```python
cap = cv2.VideoCapture(0)
```
To use a video file as input 
```python
cap = cv2.VideoCapture('filename.mp4')
```

