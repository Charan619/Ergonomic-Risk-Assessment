# Ergonomics Risk Assessment

An application developed to improve and notify users about incorrect **posture**. **Emotion** and **drowsiness** detection has been implemented using **transfer learning** to create a holistic workplace wellness app. This uses **MediaPipe** to detect posture and industry-standard **RULA**, **REBA** algorithms to detect imperfect posture. Leveraged **AWS Cognito** to implement authentication and to encrypt face recognition data. **AWS DynamoDB** has been utilised to handle emotion, drowsiness and posture data to generate workplace satisfaction report.

In order to examine and reduce risks related to the ergonomics of a person's home workstation, this project intends to create an assessment tool. It guarantees that everyone can evaluate their posture and receive assistance in correcting it in order to avoid developing musculoskeletal disorders. Based on industry-standard ergonomics assessment procedures like Rapid Upper Limb Assessment (RULA) and Rapid Entire Body Assessment, this program determines whether a person's posture is unsafe or not using live webcam video of them (REBA).

## Emotion and Drowsiness analysis

This also includes emotion and drowsiness analysis, where the software tracks your emotions over the course of the run and produces a report on your mental condition. The drowsiness detection component assists in alerting your mobile device if it determines that you are fatigued or not.

## Privacy

To ensure privacy, only your face will be tracked because live face tracking is enabled in this location. The face tracking data is securely encrypted, and the key is kept in the AWS Cognitio entries. The user can switch to private mode if he does not want to see videos or receive live feeds. and Only the coordinate data is transferred to the cloud from the camera's edge device (local computer), not the camera's video stream, which is instead transformed into coordinates. 

## Features

- Authentication using AWS Cognito
- Posture Detection and Correction
- Emotion Tracking
- Drowsiness Detection
- Face Tracking for increased accuracy
- Telegram based notification service to warn users about bad posture and drowsiness
- Report generation based on accumulated data stored in DynamoDB

<img width="962" height="874" alt="image" src="https://github.com/user-attachments/assets/6460a71a-bac9-47cb-b163-58550d428c80" />

## Run Locally

Clone the project

```bash
  git clone https://github.com/DeepanNarayanaMoorthy/Ergonomics-and-Emotion-Monitoring.git
```

Go to the project directory

```bash
  cd Ergonomics-and-Emotion-Monitoring
```

Install dependencies

```bash
  pip install -r requirements.txt
```

Start the server

```bash
  streamlit run MainApp.py
```


## File Descriptions
- **Combined.py**: Posture, emotion, drowsiness related functions
- **angle_calc.py**: Function to derive angles from MediaPipe posture data
- **cognitio_auth.py**: AWS DynamoDB and Cognito functions
- **face_train.py**: Function to create face recognition data
- **multipage.py**: StreamLit Class to implement multiple page application


## Tech Stack

**Client:** Streamlit

**Server:** Python, Tensorflow, OpenCV


<img width="1099" height="776" alt="image" src="https://github.com/user-attachments/assets/23b02aa6-03e6-480c-91e5-f3dbce1aa9fa" />


