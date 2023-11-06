# Artificial-Sign-Language
The Artificial Sign Language uses AI to translate sign language into spoken words.

# What inspired you to make this?
When we got together as a group, we learned that some of us have family members that are deaf, where that be a parent or a grandfather. In fact, one of our group members recently became partially deaf in one ear and need to use a hearing aid. These experiences made us more aware about the difficulties of deaf people to communicate with people that don’t know sign language, which is a significant percentage of the population. There is no expectation for people to learn sign language unless they know someone that deaf. With verbal languages, we can communicate through wide-spread applications like Google Translate, but with language communicate barrier between people through ASL and people who can’t, there is no just tool. 

# What does this project do?
Our project takes in a live video feed that detects hand signs in ASL and translates it into English letters and phrases in real time.  

# How did we build it?
We set up the video feed through our computer camera, and had it specifically track hand motion through cv2 library. While the video was still on, we are constantly checking if there are any hands in frame. If there are one, we generate a box around it and get the dimensions, which we use to create the image (our data). Since all the images of the hands are different sizes, we had to crop each image, proportionally resize it, and center it on a white background to have the teachable machine accurately train the AI model. We later replicated our steps to accommodate two hands as well. The way that the AI works is that we use detection and classification. Once we have the position and data points of the hand, we could classify different phrases and letters, through and generating an AI model. In other words, we would collect hundreds of images of the same sign, and generate an AI model with teachable machine. After uploading the AI model to our project folder, we, then, would use the cv2 detection capabilities to label and to detect if someone was signing the same sign in real time. 

# What challenges did we face?
We faced problems finding modules and libraries that not only supported hand tracking and could get data points for our hands, but also had extensive documentation. The most difficulty with the modules/libraries came with its compatibility with our computers. With MacOS laptops, the installed modules only went as fars as tracking our hands; however, when we turned to collecting data and having the AI translate ASL, the tensor flow installation would not work with any of the python environments we were working in. So, we finally tested our code in a windows laptop, and successfully tested our AI which correctly translated our data. Another problem we faced was collecting enough data so the AI could accurately detect the ASL signs we wanted. While testing we realized that signs would often have overlap, so the AI would misinterpret the data, meaning that we have to add more images to further train it, improving its accuracy. 

# What accomplishments are you proud of?
Though we are proud of ourselves for being able to build an AI program that is able to detect, classify, and translate sign language, the moment we were the proudest was when we got a singular image detecting two hands instead of one hand. With two hands we could now translate more phrases and form sentences from ASL to English, thus, giving us the capability of creating a whole language rather than only an alphabet. 

# What did you learn while building this?
To even begin coding this project, we had to understand what the modules and libraries could do. For example, the open cv library allowed us to track a live video feed of a hand. Using the library, we were able to get the coordinates of our hands so we could begin collecting data for our AI. We also learned about the TensorFlow library that could scale our project data and accelerate training our AI to process our collected data into words. 

# What's next for your project?
Next we would like to incorporate text to speech and expand the data in our project. With text to speech, people can communicate with one another without any barriers. Having the tools to expand data would allow the AI to reach levels of fluency in ASL and sign languages in all other languages.

# What did you build it with?
We coded this project in python. For tracking the hands we used the libraries OpenCV, Media Pipe, CV Zone, and Numpy. Then we used a teachable machine (by google) to make a keras file, so we could train our AI using our tensor flow library. 



