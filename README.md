# BioPass

One CodeDay hackathon award for best-in-class application.

A customizable web-based password manager that utilizes biometric authentication. Users will be able to select from either voice, face, or gesture authentication in order to access their various passwords. Passwords are securely stored in a centralized database using AES-256 standard encryption. 


**FILE LOCATIONS**

client folder holds the source code for the application front-end

  - TensorFlow gesture recognition is located in **Step3WebCam.tsx** in BioPass/client/comps/Layout/loginSteps/Step3/

nodeServer folder holds the TypeScript API and source code for the voice authentication and speech-to-text algorithms 

  - A new voice profile for speaker verification is enrolled into the database in **enroll.ts**
    - used when user registers a new account
  
  - Voice profile is matched against inputted audio on sign-in page in **authenticate.ts**
    - This is the main voice authentication algorithm and returns accepted or denied depending on if the inputted audio matches the previously enrolled voice profile

pythonServer folder holds the flask API and source code for the face verification algorithm

  - face profile for facial recognition is enrolled in **addPerson.py**
    - face profile is enrolled when user registers a new account
  
  - face profile is compared to inputted image in **verification.py**
    - Facial verification for sign-in page is done in this algorithm
    - Returns accepted if inputted image on sign-in matches face profile created at account enrollment
    - If image does not match, denied is sent to the front-end

## Technologies Used
  1. Python
  2. TypeScript
  3. Flask
  4. Express.js
  5. Azure
  6. MongoDB
  7. React/Next.js
  8. TensorFlow.js

## Application Demo

https://github.com/jnalbert/BioPass/assets/65417105/a810bf51-c7d1-4c0f-92ae-8ba8a7045101
