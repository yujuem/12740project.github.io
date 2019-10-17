## Introduction

GesPress is the system that would control the computer application with the motion of the hand. GesPress is consisted of the software part (Python code) and the hardware part (including sensors, A/D convertor and Raspberry Pi). Hardware part would detect the presence of the hand and collect corresponding data. While software part would perform different reactions based on the signal detected from hand motion. For now, GesPress is able to control presentation slides and music players, including local player and online portals like YouTube. 

[Project Progress](https://yujuem/12740project.github.io/Project_progress.md)


### Motivation
To control the presentation, professors make the hand available for pressing buttons, touchpad, or remote device. Team AD thought of a touchless interface composed of Raspberry Pi and sensors for hand-free presentation control. The world has been revolving around the touchless interface today and creating hand-motion control for presentations during classes was just a minuscule part of the bigger idea.

This study has focused the energies on solving real-time issues. GesPress can potentially be a part of the automated infrastructure systems and can improve the lifestyles of users. Therefore, the device can contribute to the ongoing research on cutting edge technologies.


### Goals

By the end of the project, Team AD is going to achieve:

- Designing a model to unscramble hand motions into non electrical signals -- defining the time and sequence of hand presence.

- Transferring the nonelectrical signals into electronic signals through Analog to Digital Converters (ADC) -- light signals to voltage signals.

- Processing the digital data properly -- eliminating noise, adhering to a basic standard of data quality, including the objectivity, utility, and integrity of the signals.

- Expanding the real-world application of hand motion reader -- be able to control the keyboard to control laptop under the construction read from hand motion. More specifically, the GesPress can control some basic operations like moving forward, backward and pause, when playing video or doing a presentation based on the hand motion detected.

- Creating a stable and flexible environment for the hardware -- making a box to make sure that the effect of hand motion on the sensor won't vary with the environment. 

### Methodology




### Experiments and Results

**Experiment 1: Experiments with One Sensor**

Experiment is conducted to test the photosensitive light sensors in order to implement hand-gesture based control for the project. Initially the team tested only one sensor to check the analog output and the sensor sensitivity. This was done to make sure that the light sensors could successfully capture the hand gesture. One photosensitive light sensor was connected to the Raspberry Pi. On moving our hand above the sensor, the light detected by the sensor is reduced. This corresponded to a jump in the voltage. 

**Experiment 2: Experiments with Two Sensors**

To detect a hand motion (gesture), more than one sensor is required. After the first experiment, the team added another photosensitive light sensor to the circuit. Simultaneous readings from two sensors is used to detect hand motion from right to left or left to right direction. Additionally, the setup was enclosed in a box to reduce the influence of ambient lighting on the sensors and minimise noise from ambient atmosphere (vibrations, wind, heat etc.).

**Experiment 3: Analog output I**

Experiment is conducted to make the system to detect the hand motion successfully. Two light sensors, Raspberry Pi, A/D converter, and python code are used to create the system. The difference in the analog voltage output values between the initial value and measurement is appended to the list of sensor. List has fixed length of three. Hand motion is detected in the code by comparing the first and last value of both lists.The system is not detecting the hand motion properly, and the modification of the code is needed. 

**Experiment 4: Analog output II**

Experiment is conducted modify the code used in Experiment 3 to detect the hand motion successfully. Method and Procedure are similar to Experiment 3. Unlike Experiment 3, the list does not have fixed length but have maximum length defined by time.sleep value and maximum time of hand motion. The system detects the hand motion correctly except when the hand moves quickly. 

**Experiment 5: Presentation Control**

Experiment is conducted to control the presentation with slightly modified code created in Experiment 4. Library pynput is imported to press and release the key for each hand motion. Left to right motion forwards the presentation while right to left motion backwards the presentation. Presentation slides are controlled with a hand motion successfully except when the hand moves quickly. 

**Experiment 6: Music Control**

Experiment is conducted to control the music. The system also detects the long placement of hand on each sensor and both sensors. The long placement of hand on left sensor, right sensor, and both sensors make the system to forward the music, rewind the music, and resume/pause the music. Music is controlled with a hand motion successfully except when the hand moves quickly. 

**Experiment 7: Construction of the Device Box**

The requirements for the box are:

  - It should be compact. It should be easy to disintegrate and assemble back
  
  - Provide structural support to the circuit 
  
  - Non conducting and thermally insulating 
  
  - Have opening for the sensor

To meet these requirements, the box consists of two compartments that can be easily disintegrated. The top compartment houses the entire circuit and the sensors are attached to the bottom part of the top panel. This ensures protection from ambient environment. Moreover, the box is made up of wood to prevent thermal and electric conduction.



### Discussion

**What we gain from the project?**

We implemented the hand movement control of slides and music player by using light sensors, A/D convertor and Raspberry Pi. We also uploaded our real-time data to the OpenChrip in order to create the IoT device. With the completion of the project, we get a deeper understanding of (1) the principles of various sensors, (2) the circuits analysis, (3) Linux commands and Python programing, (4) A/D conversions and signal processing.

**What can we do in the future?**

For now, the device still has some places can be improved. (1) Firstly, certain intervals are required for each movement. The sensor needs a certain period of time to initialize once it fails to detect a movement or just finish the previous detection, which sometimes results in a lack of smooth operation. (2) Secondly, the device only contains two light sensors, so we can’t enable more complex movement control. With two sensors, we could detect five types of movement at most (left-to-right, right-to-left, left-dark, right-dark, both dark). If more sensors are included in the device, we is able to explore more complex movements. However, the extraction and combination of signals will also become more difficult.

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown].
[GitHub Flavored Markdown] = https://guides.github.com/features/mastering-markdown/

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/c-sachdeva/GesPress.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
