# Brand Identifier
A simple machine learning app that can attempt to identify brands in photos. 

## How it works
This app works by allowing users to upload their own photos (or use the project's default photo files) to be analyzed by the computer vision model. The selected photo is uploaded to Cloudinary which hosts the photo and gives the file its own unique URL. 

This URL is then sent to Azure, where the computer vision model analyzes the photo and returns the brand(s) (if identified) and a confidence rating for each brand identified.

The confidence rating shows how accurate the model ranks its result as correct. If the brand(s) is not identified, the model will return a result stating no brands were found.


### Install

`npm install`

---

### Things to add
You will need to set up your own Cloudinary and Azure accounts for these next steps. You can use the free versions for this. Once you have your accounts created, set up a computer vision resource on Azure. Finally, add your Cloudinary and Azure keys into the application's `.env` file. **IMPORTANT: Make sure that your `.env` file is included in your `.gitignore` file or else people will steal your keys! **

Follow the below format to enter your keys:

- Create a config folder with a `.env` file and add the following as `key = value`
  - PORT = 2121 (can be any port example: 3000)
  - CLOUD_NAME = `your cloudinary cloud name`
  - CLOUD_API_KEY = `your cloudinary api key`
  - CLOUD_API_SECRET = `your cloudinary api secret`
  - MS_COMPUTER_VISION_SUBSCRIPTION_KEY = `your Microsoft Subscription Key`
  - MS_COMPUTER_VISION_ENDPOINT = `your Microsoft Computer Vision Endpoint`
  - MS_FACE_ENDPOINT = `your Microsoft Face Endpoint`
  - MS_FACE_SUB_KEY = `your Microsoft Face Key`

---

### Run

`npm start`
