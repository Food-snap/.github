# FoodSnap Mobile App

## Description

FoodSnap is a mobile application designed to help users identify and track their food intake through image recognition technology. The app allows users to capture or upload images of their food, recognize the food items, and get detailed nutritional information.

## Features

- **Food Recognition**: Uses machine learning to identify food items from images.
- **Nutritional Tracking**: Tracks the nutritional value of identified foods.
- **User Profiles**: Allows users to create and manage their profiles.
- **History Log**: Keeps a history of all recognized food items and their nutritional information.

## Getting Started

To set up the project locally, follow these steps:

1. Clone the repository:
    ```sh
    git clone https://github.com/Food-Snap/mobile-app.git
    ```
2. Navigate to the project directory:
    ```sh
    cd mobile-app
    ```
3. Copy `local.properties.example` to `local.properties`:
    ```sh
    cp local.properties.example local.properties
    ```
4. Update the configuration values as needed.
5. Open the project in Android Studio.
6. Ensure you have the required dependencies and SDK versions installed.

## Screenshots

<div style="display: flex; justify-content: space-between;">
  <img src="https://github.com/Food-Snap/.github/blob/main/screenshots/Splash%20Screen.png?raw=true" width="24%">
  <img src="https://github.com/Food-Snap/.github/blob/main/screenshots/OnBoading.png?raw=true" width="24%">
  <img src="https://github.com/Food-Snap/.github/blob/main/screenshots/Login.png?raw=true" width="24%">
  <img src="https://github.com/Food-Snap/.github/blob/main/screenshots/SignUp.png?raw=true" width="24%">
</div>
<div style="display: flex; justify-content: space-between;">
  <img src="https://github.com/Food-snap/.github/blob/main/screenshots/Home.png?raw=true" width="24%">
  <img src="https://github.com/Food-Snap/.github/blob/main/screenshots/History.png?raw=true" width="24%">
  <img src="https://github.com/Food-Snap/.github/blob/main/screenshots/Food%20Detail.png?raw=true" width="24%">
  <img src="https://github.com/Food-Snap/.github/blob/main/screenshots/Profile.png?raw=true" width="24%">
</div>
<div style="display: flex; justify-content: space-between;">
  <img src="https://github.com/Food-Snap/.github/blob/main/screenshots/Edit%20Profile.png?raw=true" width="24%">
  <img src="https://github.com/Food-Snap/.github/blob/main/screenshots/Edit%20Password.png?raw=true" width="24%">
</div>

## Demo Video

Watch the demo video of the FoodSnap app [here](https://drive.google.com/file/d/1RkIp1k_FHemZIlby4MZAE4AlIQDg_dXA/view).

## Download APK

You can download the APK of the FoodSnap app [here](https://drive.google.com/file/d/1K25aRTqfpeLFgQlQZAHBfW1JKvD2fJqd/view).

# FoodSnap Backend Service
This repository contains the backend service for the FoodSnap application. The backend service is built with Node.js, Express, and deployed on Google Cloud App Engine. It handles user authentication, food prediction, and history tracking.

## Table of Content
1. Prerequisites
2. Installation
3. Running the Application Locally
4. Deployment
5. API Endpoints
6. Environment Variables

## Prerequisites
* Node.js (14 or higher)
* npm (6 or higher)
* Google Cloud Project with App Engine, Cloud Storage, Firestore enabled

## Installation
1. Clone the repository
   ```
   git clone https://github.com/your-username/foodsnap-backend.git
   cd foodsnap-backend
   ```
2. Install Dependencies
   ```
   npm install
   ```
3. Create a .env file in the root directory and add the following environment variables
   ```
   GCLOUD_PROJECT_ID=your_gcloud_project_id
   GCLOUD_KEY_FILE=/path/to/serviceAccountKey.json
   GCLOUD_STORAGE_BUCKET=your_gcloud_storage_bucket_name
   JWT_SECRET=your_jwt_secret
   PORT=8080
   ```

## Running the Application Locally
1. Start the application
   ```
   npm run start
   ```
2. Access the application
   Open your browser and navigate to http://localhost:8080

## Deployment
1. Activate Cloud App Engine
2. Create app.yaml file
3. Deploy using Google Cloud CLI
   ```
   gcloud app deploy
   ```

## API Endpoints

### Auth
* POST /signup - Register a new user
* POST /login - Authenticate a user and return a token

### User
* GET /profile - Get the user profile
* PUT /edit-profile - Update the user profile
* PUT /change-password - Change the user password

### Food
* GET /food - Get the list of food
* GET /food/{id} - Get Food Detail with id

### Predict
* POST /predict - Preduct the food image and return food data

### History
* GET /history - Get the user's food history
* POST /save - Save the prediction result to history

## Environment Variables
Make sure to set the following environment variables in your .env file or through your deployment platform:
* GCLOUD_PROJECT_ID : your Google Cloud Project ID
* GCLOUD_KEY_FILE : Path to your Google Cloud Service Account Key
* GCLOUD_STORAGE_BUCKET: Name of your Google Cloud Storage Bucket
* JWT_SECRET : Secret key for JWT authentication
* PORT : Port in which the app will run (default is 8080)

