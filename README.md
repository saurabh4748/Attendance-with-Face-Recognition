# Attendance-with-Face-Recognition

## Libraries used:
 
   CMake: <br> CMake is cross-platform free and open-source software for build automation, testing and packaging using a compiler-independent method. CMake is not a build system but rather it's a build-system generator.
  <br> Dlib:<br> Dlib is a general purpose cross-platform software library written in the programming language C++. Its design is heavily influenced by ideas from design by contract and component-based software engineering. 
  <br> Face-recognition:<br> Recognize and manipulate faces from Python or from the command line with the world’s simplest face recognition library. Built using dlib’s state-of-the-art face recognition built with deep learning.
 <br> NumPy:<br> NumPy is a Python library used for working with arrays. It also has functions for working in domain of linear algebra, Fourier transform, and matrices.
 <br> OpenCV:<br> OpenCV (Open Source Computer Vision Library) is an open source computer vision and machine learning software library. OpenCV was built to provide a common infrastructure for computer vision applications and to accelerate the use of machine perception in the commercial products.

## Process of face-recognition :
 
  Step 1: <br>Finding all the Faces
    We’re going to use a method called Histogram of Oriented Gradients — or just HOG for short.
    To find faces in an image, we’ll start by making our image black and white.
    Then we’ll look at every single pixel in our image one at a time.
<br>
  Step 2:<br> Posing and Projecting Faces :
    We are going to use an algorithm called face landmark estimation.
    The basic idea is we will come up with 68 specific points (called landmarks) that exist on every face — the top of the chin, the outside edge of each eye, the inner edge of     each eyebrow, etc. Then we will train a machine learning algorithm to be able to find these 68 specific points on any face.
    <br>
  Step 3:<br> Encoding Faces
    This process of training a convolutional neural network to output face embedding requires a lot of data and computer power.
    So we run our face images through their pre-trained network to get the 128 measurements for each face
    <br>
  Step 4: <br> Finding the person’s name from the encoding:
    Now we have to do is find the person in our database of known people who has the closest measurements to our test image.
    We can do that by using any basic machine learning classification algorithm. We’ll use a simple linear SVM classifier.
    All we need to do is train a classifier that can take in the measurements from a new test image and tells which known person is the closest match. Running this classifier       takes milliseconds. The result of the classifier is the name of the person!

## CONCEPT OF FACE RECOGNITION
   Pictures have a hierarchy or conceptual structure. our neural network can’t do this. It thinks that an “8” in a different part of the image is an entirely different thing.       It doesn’t understand that moving an object around in the picture doesn’t make it something different. This means it has to re-learn the identify of each object in every         possible position. We need to give our neural network understanding of translation invariance — an “8” is an “8” no matter where in the picture it shows up.

   <br>We’ll do this using a process called Convolution. The idea of convolution is inspired partly by computer science and partly by biology.
    <br>Instead of feeding entire images into our neural network as one grid of numbers, we’re going to do something a lot smarter that takes advantage of the idea that an           object is the same no matter where it appears in a picture.
    <br>The solution is to train a ###Deep Convolutional Neural Network. 

