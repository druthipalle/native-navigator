# native-navigator

What it does:
Native Navigator was created to assist new drivers and/or foreign drivers in reading common street signs. The user inputs an image of a street sign and selects a language of their choice. The AI then identifies what street sign it is and outputs an mp3 file that translates the sign in their desired language. 

How we built it:
We began the project by using LabelBox to label our data. In order to fully train the data, we needed at least 100 images per street sign. We obtained our data by downloading images from the web. To gather a wider range of data, we augmented several images from the web by rotating, flipping, and modifying their brightness. We were able to create 27 different variations of each image, which drastically increased the accuracy of our product. After gathering all of our data we sorted all of the images into their respective categories with the help of LabelBox. We submitted nearly 1,500 images into LabelBox separating them into 10 unique categories (stop sign, road work ahead, school zone sign, left turn only, yield sign, right turn only, one-way sign, U-turn sign, no parking, winding road). After labeling all the data, we began training the data using Yolo which took approximately 2 days.  First, we initialized random weights in our neural network and made forward passes through the network with our training data. From this, we calculated the loss and used gradient descent to identify which weights needed to be changed and by how much. We distributed the weight changes with the use of back propagation. We continued to repeat training until we were satisfied with the loss. After training our data we created a confusion matrix to view our accuracy rates. We then worked on the Google Speech translate API. First, the google text-to-speech API analyzes a python string that is received after the AI identifies a sign. The API then recognizes the words in the string and converts them into a language that would be given as an input. Lastly, an mp3 file is created and a human-like voice will say the name of the sign in the language chosen by the user. After completing all the different aspects of our project we worked on creating our webpage. On the front end, we used NicePages to add various features such as buttons, drop-downs, images, and the overall framework. On the back end, we used Flask, a library in Python, to generate the website. We used HTML, JavaScript, and CSS to format the contents on the webpage. After completing the website we deployed our project with the help of the AI Camp team. 

Challenges we ran into
Accomplishments that I'm proud of 
What's next to Native Navigator
Built with
Try it out: https://native-navigator.ai-camp.org/
Presentation: https://docs.google.com/presentation/d/1l29LAgqp9RP15bCoWcsvJnuOSqpdgObtfOvwCnkQxKg/edit?usp=sharing
https://www.youtube.com/watch?v=B8ee8V7qp-4&t=16s
