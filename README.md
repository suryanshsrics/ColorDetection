# ColorDetection

## Introduction

Color detection plays a crucial role in computer vision applications. This color detection model utilizes the OpenCV library to process images and identify various colors present within them. The model is built using a machine learning algorithm and can accurately recognize colors based on their RGB values.


## The Dataset

Colors are made up of 3 primary colors; red, green, and blue. In computers, we define each color value within a range of 0 to 255. We will be using a dataset that contains RGB values with their corresponding names. The CSV file for our dataset has been added in the `Dataset` section of this repository. The `colors.csv` file includes 865 color names along with their RGB and hex values.


## Prerequisites

* OpenCV
* Pandas
* NumPy


## Steps for building the project

### Taking an image from the user: 
The `argaparse` library is used to create an argument parser. We will directly give an image path from Command Prompt.

### Read the csv file with Pandas
The `pandas.read_csv` function is used to read the csv file into a Pandas dataframe

### Set a mouse callback event on a window
First, we have created a window in which the input image will be displayed. Then, we set a callback function which will be called when a mouse event happens.

### Create the draw_function
It will calculate the rgb values of the pixel which we double click.

### Calculate distance to get color name
We have the r,g and b values. Now, we need another function which will return us the color name from RGB values. To get the color name, we calculate a distance(d) which tells us how close we are to color and choose the one having minimum distance.
  
Our distance is calculated by this formula:
  
d = abs(Red – ithRedColor) + (Green – ithGreenColor) + (Blue – ithBlueColor)

### Display image on the window
Whenever a double click event occurs, it will update the color name and RGB values on the window.

### Run Python File
The beginner Python project is now complete, you can run the Python file from the command prompt. Make sure to give an image path using ‘-i’ argument. If the image is in another directory, then you need to give full path of the image:

python color_detection.py -i <add your image path here>


## Some Examples

![image](https://github.com/suryanshsrics/ColorDetection/assets/118303765/8f6b6925-d6d0-4675-ad88-f9928a92b6a9)



![Screenshot (69)](https://github.com/suryanshsrics/ColorDetection/assets/118303765/87d3e0e8-e26d-44f1-9ceb-185289427880)




![Screenshot (68)](https://github.com/suryanshsrics/ColorDetection/assets/118303765/aacb9b90-9d41-40c7-a752-6275e445a550)

