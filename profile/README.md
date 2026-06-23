# 💡 Project ARIS: Automated Rearing Intelligent Sensing
Project ARIS is an autonomous robotic system that feeds bumblebee larvae. 
The project, and this readme not final! Every repo has its own readme with more specific information.
<!-- cool project cover image -->
![Project Cover Image](/media/chosenlogo_cropped.png)

<!-- table of content -->
## Table of Contents
- [The Team](#the-team)
- [Project Description](#project-description)
- [Getting Started](#getting-started)
- [Prerequisites](#prerequisites)
- [Installing](#installing)
- [Testing](#testing)
- [Deployment](#deployment)
- [Built With](#built-with)
- [Acknowledgments](#acknowledgments)

## 👥 The Team 
**Team Members**
- [Nitai Gildor](mailto:nitai.gildor@mail.huji.ac.il)
- [Asaf Shasha](mailto:asaf.shasha@mail.huji.ac.il)

**Supervisors**
- Mentor: [Daniella Har Shalom](mailto:daniellah@gmail.com)
- Moderator: [Professor Guy Bloch](mailto:guy.bloch@mail.huji.ac.il)
- Affiliation: Professor Guy Bloch Group, Alexander Silberman Institute of Life Science, The Hebrew University of Jerusalem.

## 📚 Project Description
Manual rearing of bumblebee larvae for research is labor-intensive and produces inconsistent results, severely limiting the scale and reproducibility of experiments. Researchers studying sociality and caste differentiation require precisely calibrated feeding and consistent schedules that current manual methods cannot sustain. 

ARIS is an integrated robotic platform designed to automate larvae rearing with high precision. The system synchronizes three core capabilities: real-time larval size estimation, a precision microfluidic delivery system, and a motion platform for accurate positioning.

**Main Features & Functionalities:**
* **Autonomous Navigation:** The system demonstrates successful autonomous spatial navigation over a grid of larvae wells.
* **Intelligent Size Estimation:** A primary feature is evaluating food amounts based on volume and height estimation from 2D images. 
* **IR Vision Supplement:** To avoid disrupting development, the system utilizes active IR lighting and high-contrast backgrounds to enhance the larva's silhouette.
* **Touch-Dispensing Mechanism:** Overcomes physical challenges with micro-volumes (where capillary forces prevent droplets from detaching) by maneuvering the tip to "smear" the food droplet directly onto the larva.

**Main Components:**
* **3D Motion Control:** Robotic arm for delicate, spatial manipulation.
* **Fluidics System:** Microfluidics for accurate, micro-volume nutrient delivery.
* **Vision System:** Computer vision for precise larva sizing and location detection.
* **Control Unit:** Central system integrating a custom UI to schedule and manage operations.


[//]: # (## ⚡ Getting Started)

[//]: # ()
[//]: # (These instructions will give you a copy of the project up and running on your local machine for development and testing purposes. *Note: As Project ARIS spans multiple repositories, please refer to the specific module's README for exact software installation commands.*)

### 🧱 Prerequisites
Software:
- Windows 11 (Project not verified on other OS version)
- Python 3.12 (Project not verified on other interpreters)
- Dependencies detailed in every repo's README

Hardware:
- Tevo Tornado: 3-axis motion system (Modified 3D printer gantry). Note: While our software may run on other 3D printers, we only verified and calibrated on the Tevo Tornado.
- Chorny BT100M Peristaltic Pump.
- Arduino Uno welded to a 15 pin cable according to our welding map (will be uploaded later)
- Rasberry pi zero 2 + IMX219 camera sensor

[//]: # (### 🏗️ Installing)

[//]: # (A step-by-step series of examples that tell you how to get a development environment running:)

[//]: # ()
[//]: # (1. Clone the organization repositories relevant to the subsystems you are testing &#40;Motion, Fluidics, Vision, or Control&#41;.)

[//]: # (2. Establish hardware connections between the 3-axis motion system, the precision peristaltic pump, and the central control unit.)

[//]: # (3. Launch the ARIS Control Unit UI via your Python environment.)

[//]: # (4. Prepare the physical environment:)

[//]: # (    * Place larvae plates in designated areas.)

[//]: # (    * Connect the food container to the fluidics system.)

[//]: # (    * Insert the feeding program using the custom UI.)

[//]: # ()
[//]: # (Once running, the automated cycle will sequentially move above the larva, analyze its size and height to calculate food amounts, move down to accurately dispense the calculated food, and save the feeding amount and picture for data insights before continuing.)

## 🧪 Testing
We have established quantitative metrics to evaluate the system's core functionalities. Testing should be conducted against these benchmarks:

### Sample Tests
* **Feeding Precision:** Evaluates the accuracy of the microfluidic delivery. The target is to achieve a feeding volume error of less than 10% of the required volume.
* **Larval Size Detection:** Evaluates the Computer Vision (CV) accuracy. Compare the algorithmic outputs of larva volume and height to manual measurements, targeting an error margin under 10%.
* **Functional Reproducibility:** Simulates weekend operations. Ensure continuous operation on 24 larvae for 3 full days without human intervention.

## 🚀 Deployment
Ensure that the final deployment environment adheres to biological safety standards. Success is defined by accurate dosing with no physical damage to any larvae during operation.

## ⚙️ Related Work
  - [Design of an automated robotic microinjection system for batch injection of zebrafish embryos and larvae](https://doi.org/10.1038/s41378-023-00645-6) - Established principles for delicate handling.
  - [Flyspresso](https://doi.org/10.1038/s41598-021-89676-5) - Demonstrated practical use of syringe pumps integrated with motion stages.
  - [Regression Convolutional Neural Network (RegCNN)](https://www.researchgate.net/publication/375186762) - Proven accurate for monitoring and measuring insect larva size.

## 🙏 Acknowledgments
  - The Professor Guy Bloch Group at the Alexander Silberman Institute of Life Science for their academic support and guidance.
  - Maayan, Lab Manager, for her continuous assistance with facility and equipment coordination.