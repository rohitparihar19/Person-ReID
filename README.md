https://drive.google.com/drive/folders/1EO_BYnktTNKoDcfxBdZEPzIkahy1j0sc?usp=sharing

# Person ReID
 Person Detection and Tracking using YOLO V5 and Reid Model
Rohit Parihar
May 2022
Introduction
Person re-identification (re-id) aims to match people across non-overlapping camera views distributed at distinct locations.
![image](https://user-images.githubusercontent.com/102134613/171332538-9c67bced-111c-4f62-bab0-e1d7ed7ef09d.png)

 


Multiple Person Tracking Framework

•	Detection
•	Re-identification
•	Tracking

Person Detection
Object detection is an advanced form of image classification where a neural network predicts objects in an image and points them out in the form of bounding boxes.
Object detection thus refers to the detection and localization of objects in an image that belongs to a predefined set of classes (Person).
Tasks like detection, recognition, or localization find widespread applicability in real-world scenarios, making object detection (also referred to as object recognition) a very important subdomain of Computer Vision.
We are going to use Yolo V5 for the detection. The YOLO algorithm works by dividing the image into N grids, each having an equal dimensional region of S * S. Each of these N grids is responsible for the detection and localization of the object it contains.
•	YOLO Architecture:
Inspired by the Google Net architecture, YOLO’s architecture has a total of 24 convolutional layers with 2 fully connected layers at the end. 
![image](https://user-images.githubusercontent.com/102134613/171332487-130da5af-cbe8-477e-8c81-c6ada56aa6dc.png)


 




Re-Identification
Person re-identification (ReID), identifying a person of interest at other time or place, is a challenging task in computer vision. Its applications range from tracking people across cameras to searching for them in a large gallery, from grouping photos in a photo album to visitor analysis in a retail store. 
Reference:
AlignedReID: Surpassing Human-Level Performance in Person Re-Identification (Xuan Zhang et al.,2017)
In Defence of the Triplet Loss for Person Re-Identification
•	AlignedReID extracts a global feature that is jointly learned with local features
•	Local feature learning performs an alignment/matching by calculating the shortest path between two sets of local features
•	Global feature learning benefits greatly from local features
•	After the joint learning, only need a global feature to compute the similarities between images.
![image](https://user-images.githubusercontent.com/102134613/171332441-046b7466-a140-4c1b-977f-0d133b6bb47c.png)

 

For ReID we use Models with Triplet Loss from AlignedReID: Surpassing Human-Level Performance in Person Re-Identification (Xuan Zhang et al.) Usually, in supervised learning, we have a fixed number of classes and train the network using the SoftMax cross entropy loss. However, in some cases, we need to be able to have a variable number of classes. In people recognition, for instance, we need to be able to compare two images of unknown people and say whether they contain the same person or not.




Process Diagram
![image](https://user-images.githubusercontent.com/102134613/171332402-2cfda115-687d-4892-861c-c7a6bbddf265.png)

 


ML Pipeline
•	Getting frames from the live video stream 
•	Passing it to the person detection model 
•	Getting the bounding box location of detected Persons, cropping those detected persons
•	Passing the cropped images to the Reid model for re-identification
•	Generating IDs and visualizing them on the frame


Timeline: 3 weeks



