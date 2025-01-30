List of Contents

Introduction

Working

Installation

Dataset Creation

Introduction

(Back to top)

Plant disease detection plays a crucial role in agriculture, as diseases can severely impact plant health, productivity, and yield quality. If not addressed promptly, plant diseases can cause large-scale damage, affecting farmers and the agricultural industry.

GreenLeaf-Diagnoser is an automated system for detecting plant diseases using image processing and machine learning techniques. This tool assists farmers and plant caretakers in identifying infections at an early stage, enabling timely intervention. By leveraging machine vision, it provides an accurate, efficient, and scalable alternative to traditional manual inspection methods.

The system uses image processing algorithms to segment diseased areas from leaves and employs machine learning models to classify plant health. With this approach, early disease identification becomes possible, allowing farmers to take appropriate control measures while minimizing environmental risks.

Working

(Back to top)

The disease detection process involves multiple steps:

Image Acquisition: Collect RGB images of plant leaves.

Color Transformation: Convert RGB images to HSI format for better analysis.

Green Pixel Masking: Identify and filter out healthy green pixels to focus on affected areas.

Segmentation: Extract diseased regions by filtering out irrelevant parts (such as leaf veins or background noise).

Feature Extraction: Analyze leaf attributes like infected area percentage and perimeter.

Classification: Use a Support Vector Machine (SVM) model to classify leaves as healthy or diseased.

Why HSI Color Model?

HSI (Hue, Saturation, Intensity) is used because it aligns well with human perception. The Hue component alone provides crucial information about color variations, making it ideal for detecting infected regions.

Installation

(Back to top)

Follow these steps to install GreenLeaf-Diagnoser:

Clone the repository and navigate to the project directory:

git clone https://github.com/your-repo/GreenLeaf-Diagnoser.git
cd GreenLeaf-Diagnoser

Install dependencies:

pip install -r requirements.txt

Run the application:

python main.py

Dataset Creation

(Back to top)

To create a dataset for training and testing, use the following commands in the dataset_creator directory:

For images of the same category (e.g., all infected leaves):

python dataset_single_category.py -i .

For a mixed dataset (healthy and infected leaves):

python dataset_mixed.py -i .

Note: The script processes .jpg, .jpeg, and .png images by default. Additional formats can be added by modifying the condition in line 52 of the respective script.

With GreenLeaf-Diagnoser, early and automated plant disease detection becomes feasible, helping farmers maintain healthy crops and optimize agricultural yield.
