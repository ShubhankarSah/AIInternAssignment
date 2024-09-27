📸 Object and Text Detection with YOLOv8 and Tesseract OCR

This repository provides an end-to-end solution for object detection using YOLOv8 and text extraction using Tesseract OCR. It automatically crops and saves each detected object and text as individual masked images and creates a summary in a CSV file with descriptions of the detected entities.

📑 Table of Contents
🚀 Project Overview
📂 Directory Structure
📋 Requirements
📥 Installation
⚙️ Usage
📊 Sample Output
🔮 Future Work
🚀 Project Overview
This project builds an AI pipeline that:

Detects objects in images using YOLOv8.
Extracts text from images using Tesseract OCR.
Masks and saves detected objects and text as individual images.
Generates a summary table in CSV format, providing object labels, filenames, and brief descriptions.
📂 Directory Structure
bash
Copy code
📦 object-text-detection/
├── images/                   # Directory containing input images
│   ├── image1.png            # Example input image
│   └── image2.png
├── results/                  # Directory where outputs are saved
│   ├── object_summary.csv     # CSV summary of detected objects and text
│   ├── object_0_dog.png       # Cropped image of detected object (dog)
│   └── text_0_hello.png       # Cropped image of detected text ("hello")
├── requirements.txt          # List of required Python packages
└── object_detection.py        # Main Python script for object and text detection
📋 Requirements
The project requires Python 3.8+ and the following packages:

torch (for YOLOv8 object detection)
opencv-python (for image processing)
pytesseract (for OCR text extraction)
pandas (for summary table generation)
You will also need Tesseract OCR installed on your system. If you're using Google Colab, you can install it via:

bash
Copy code
!sudo apt install tesseract-ocr
For a complete list of dependencies, refer to the requirements.txt.

📥 Installation
Follow these steps to set up and run the project:

Clone the repository:

bash
Copy code
git clone https://github.com/your-repo-name/object-text-detection.git
cd object-text-detection
Install the required Python packages:

bash
Copy code
pip install -r requirements.txt
Ensure Tesseract OCR is installed on your machine. You can install it here.

⚙️ Usage
Running the Detection Pipeline
Place the input images in the images/ directory.

Run the main Python script:

bash
Copy code
python object_detection.py
The script will:

Detect objects in the images using YOLOv8.
Extract text using Tesseract OCR.
Save each detected object and text as individual images in the results/ folder.
Generate a object_summary.csv file summarizing all detected objects and text.
Example
python
Copy code
# Example usage in Python
python object_detection.py --source images/image1.png --output results/
📊 Sample Output
After running the script, the results/ directory will contain:

Cropped images of detected objects and text.
A summary table in CSV format, e.g., object_summary.csv.
Example Summary Table:
ID	Label	Description	File Name
1	Dog	Detected a dog in the image	object_1_dog.png
2	Text	Detected text: "hello"	text_2_hello.png
The cropped images will be saved with filenames like object_1_dog.png and text_2_hello.png.

🔮 Future Work
Possible improvements for the project include:

Action and Emotion Detection: Use pre-trained models to describe human actions and emotions in the image.
Detailed Object Classification: Expand object detection to include specific breeds, categories, or brands.
Improved Text Detection: Use more sophisticated OCR techniques to enhance text extraction accuracy.
