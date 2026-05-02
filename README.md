# Store_Image

A web app my partner and I built that lets users upload images and get AI-generated labels back describing what's in them. Built using AWS S3 for storage and AWS Rekognition for the labeling.

## What It Does

Users can upload an image through the browser. The image gets stored in an S3 bucket, then Rekognition analyzes it and returns labels with confidence scores. Those labels get displayed back to the user. If Rekognition doesn't detect anything, the app shows a "No Labels" category instead of just breaking.

We also added retry logic so the image processing doesn't fail silently if something goes wrong on the AWS side.

## Tech Used

- Python (boto3 for AWS integration)
- JavaScript, HTML, CSS
- AWS S3
- AWS Rekognition

## How to Run It

### What you need
- Python 3.x
- An AWS account with S3 and Rekognition access
- boto3

```bash
pip install boto3
```

### AWS setup

```bash
aws configure
```

Enter your AWS access key, secret key, and region when prompted.

### Running the app

```bash
git clone https://github.com/YOUR_USERNAME/store-image.git
cd store-image
python app.py
```

Then open index.html in your browser.

## File Structure

```
store-image/
├── app.py        
├── index.html    
├── style.css     
└── script.js     
```

## About

Built by Kaleb Chaney — CS student at Northwestern University, class of 2027.
GitHub: github.com/YOUR_USERNAME
