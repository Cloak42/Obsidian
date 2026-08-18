---
tags:
  - template
---
---
GitHub Repository:https://github.com/Cloak42/IMU-Tests

---
## Intro/Concept:
---
## Brainstorm Ideas
- [ ] 
---
## Time Line:
- [ ] 
---
## Concept Drawings/Notes:

---
## File ledged

| File Name                      . | File Description                 .                                                                                           |
| -------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| IMUReadOut.ino                   | displays the raw data from the accelerometers and the gyroscopes to serial                                                   |
| PitchRollReadOut.ino             | converts raw accelerometer and gyroscope data into pitch and roll degree values                                              |
| zerodIntPitchRoll.ino            | same as PitchRollReadOut.ino but integrates an offset value taken at start up, truncates the pitch and roll values into ints |
| mapRoll.ino                      | maps the roll values to values between -2 and 2                                                                              |
| basicLightLevel.ino              |                                                                                                                              |

---
## Component Guide

| Component name/number | Component type | Component use/assosiated part |
| --------------------- | -------------- | ----------------------------- |
| BMI160                | IMU module     |                               |

---
## BMI160 Description and Use

wiring diagram:
![[Pasted image 20260817160252.png|618]]

Arduino Library: https://github.com/DFRobot/DFRobot_BMI160

---
## Results/ updates

---