Le Pipeline
===========

Headset Detection:
------------------

Model Used: YOLOv11 (You Only Look Once, version 11).
Function: Detects whether a headset is being worn by the worker.
Process: The model processes the video feed and identifies the presence or absence of a headset near a worker’s head.


Phone Detection:
------------------

Model Used: YOLOv11.
Function: Detects the presence of a phone near a worker’s face.
Process: The model identifies when a phone is being held close to the face, indicating potential distractions.


Drowsiness Detection:
------------------

Model Used: Mediapipe Face Mesh.
Function: Monitors worker drowsiness based on facial landmarks.
Process:
Calculates the distance between the upper and lower eyelids to detect if eyes are closing.
Measures the distance between the lips to check for yawning.
Combines these metrics to determine if the worker is drowsy.


Face Calibration:
------------------

Model Used: Face recognition library with a pre-trained model and a pickle file of unique faces.
Function: Identifies and tracks workers uniquely.
Process: Compares detected faces against the stored database of unique faces to ensure accurate monitoring.
Alert System
The project includes an alert system to notify supervisors of any persistent issues:


Conditions That Trigger Alerts:
------------------

Drowsiness detected continuously for a specific period.
No headset detected for a defined period.
Phone detected near the face for a prolonged time.


Alert Mechanism:
------------------

When a condition is detected, a timer starts.
If the condition persists beyond a set threshold, an alarm is triggered.
Alerts can include a sound, visual notification, or a message to the supervisor's dashboard.


Why Use Delayed Alerts:
------------------

Prevent false alarms due to brief or accidental behaviors.
Ensure that only sustained issues raise alerts.

This system ensures a balance between worker comfort and maintaining focus in the call center.

















