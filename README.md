# YOLOv8 Traffic Light Detection 🚦

## Project Overview

This project is a real-time traffic light detection and classification model designed to enhance the visual perception capabilities, which is one of the most critical components of autonomous driving systems. Developed as a term project for the Artificial Intelligence course at Sivas Cumhuriyet University, this study bridges theoretical machine learning concepts with practical computer vision applications to create a working product.

**Dataset and Challenges**
The **BDD100K** dataset, a global industry standard in autonomous driving projects, was used to train the model. The primary reason for choosing this massive 7.6 GB dataset was to test the model in challenging real-world scenarios such as night driving, rainy weather, windshield reflections, and heavy urban traffic.

A rigorous data preprocessing phase was conducted prior to training. Thousands of labels within the complex JSON structures of BDD100K were parsed using a custom script. Only the traffic light coordinates were extracted and converted into the normalized format (`center_x, center_y, width, height`) required by YOLO. The system is designed to detect three main classes: Red, Green, and Yellow.

**Training Process and Performance Improvement**
The YOLOv8 architecture, known for its speed and accuracy in object detection, was chosen for this task. The model underwent intensive training for 50 epochs using a Tesla T4 GPU. Early stopping techniques were applied to prevent the model from memorizing the training data (overfitting).

As a result of this extended training, the model's overall Precision score reached **74.3%**, successfully minimizing false positives, such as mistaking circular red signs or vehicle brake lights for traffic signals. The most significant achievement was observed in the "Yellow Light" class, which had a severe lack of data instances. The yellow light detection performance (mAP50), which was initially at 19.9% in early stages, surged to **52.5%** after the optimizations, largely resolving the class imbalance problem.

## Author

**H. Can Umutlu**<br>
*Information Systems and Technologies* <br>
*Sivas Cumhuriyet University*<br>
<a href="https://www.linkedin.com/in/himmetcanumutlu"><b>Connect With Me On LinkedIn</b> </a>

## License

This project is released to the open-source community under the **MIT License**. This licensing model grants you full freedom to review the code in this repository, integrate it into your personal or commercial systems, and make any modifications you desire. The software is provided "as is"; for detailed legal boundaries and the disclaimer of liability, please review the LICENSE file included in the project.
