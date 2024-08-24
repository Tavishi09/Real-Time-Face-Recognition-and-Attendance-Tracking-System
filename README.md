# Real-Time-Face-Recognition-and-Attendance-Tracking-System
Face Attendence Project
Overview
We have created a face attendance project using python, Open CV, and Face recognition that will use webcam to detect faces and record the attendance. It will take an unknown image as an input and give a labeled image as output.

# Packages Involved
• cmake 
• dlib 
• face_recognition 
• Numpy 
• Opencv

# Process Involved
1. Image importing to database and coverting to RGB
2. Find faces location and compute encodings
3. Compare faces
4. Labelling faces

  
1. Image importing to database and coverting to RGB:
First we load the images into our database,import relevant libraries and convert it to RGB .

2. Find faces location and compute encodings:
Here we use face recognition library to find faces in our image using histogram HOG of orientated gradients and we remove the rotations and feed it to a neural network that puts it into 128 measurements that are unique to a particular face.

3. Compare faces:
now we compare two faces to find similarities by using compare_faces function to find if the faces match.The function used here returns true or false.We also use Face_distance to find how likely the faces match in terms of numbers.

4. Labelling faces:
After doing the importing images ,converting it to RGB and computing encodings;we take an image as an input from the webcam then resize it to find the faces in it.Then we compare it with the faces in our database ,then we find the best match in case more than once face is detected at a time. Now we determine the name of the person and display it on the original image. We will start by writing a function that requires only one input which is the name of the user. First we open our Attendance file which is in csv format. Then we read all the lines and iterate through each line using a for loop. Next we can split using comma ‘,’. This will allow us to get the first element which is the name of the user. If the user in the camera already has an entry in the file then nothing will happen. On the other hand if the user is new then the name of the user along with the current time stamp will be stored. We can use the datetime class in the date time package to get the current time. Also if the image in not in our database then it also labels it as Unknown. Output We have input the Elon Musk image in our code and then give a sample input images of Elon Musk & Bill Gates for recognition then it will return the labeled image as true or false.

  # Output
We have input the Elon Musk image in our code and then give a sample input images of Elon Musk & Bill Gates for recognition then it will return the labeled image as true or false.

input image in code
<figure>
    <img src="Elon-Musk.jpg" alt="Image">
    <figcaption align="center">Input Image In Code </figcaption>
</figure>

output
TRUE
<figure>
    <img src="Elon2-1.jpg" alt="Image">
    <figcaption align="center">
</figure>

FALSE
<figure>
    <img src="Elon2-2.jpg" alt="Image">
    <figcaption align="center">
</figure>
