# About the project
### Defect Detection for Quality Assurance in Industrial Manufacturing
Welcome to my Capstone Project, a machine learning initiative focused on tackling the critical challenge of defect detection in industrial manufacturing processes!

### Motivation: 
Traditional quality assurance (QA) methods often struggle to catch subtle defects and lack real-time monitoring capabilities. This can lead to significant financial losses, reputational damage, and dissatisfied customers. To address this, I've developed a novel machine learning approach that empowers manufacturers with:

### Early defect detection: 
Identifying imperfections early in the production line minimizes financial losses and product recalls.
Enhanced brand image: Consistent quality control safeguards your brand reputation and fosters customer trust.
Improved process optimization: Precise defect classification assists in pinpointing production bottlenecks and optimizing future operations.

![Capstone_Piya_Defect Detection for Quality Assurance in the Industrial Manufacturing Process](https://github.com/pia-piyanutnithi/defect-detection-for-QA/assets/143199969/a18d4bbe-5538-4710-8711-d61c38a7654a)
*The picture visualizes the overwhelming and manual tasks the employees are facing due to a lack of proper tools.*

### Solution Overview: 
My project presents a multi-stage defect detection model, offering tailored solutions to meet diverse manufacturing needs. Each stage leverages specific machine learning algorithms and delivers increasing levels of detail, allowing manufacturers to customize the model based on their unique requirements and cost considerations.

### Project Highlights:

**Modular design:** The three-stage approach allows manufacturers to choose the level of detail needed, balancing accuracy with resource requirements.
**Algorithm flexibility:** Each stage employs the most appropriate machine learning algorithm, maximizing effectiveness and efficiency.
**Customizable options:** The model can be tailored to specific product types and defect categories, ensuring a targeted solution.
Looking Ahead:

![Capstone_Piya_Defect Detection for Quality Assurance in the Industrial Manufacturing Process (1)](https://github.com/pia-piyanutnithi/defect-detection-for-QA/assets/143199969/54aa0232-2e7a-4ec7-a715-e2398bc59267)
*Three stages of my capstone project.*

### Stage 1: Binary Classification - "Does the image have any defect?"

This initial stage acts as a powerful screening tool, employing a binary classification model to efficiently flag potential anomalies. This is ideal for initial quality checks and can be implemented even with limited resources.

The result from this stage is impressive. I used ROC Curve to evaluate the model and it returned 96% accuracy. The result provides reliability of the model. 
![Capstone_Piya_Defect Detection for Quality Assurance in the Industrial Manufacturing Process (2)](https://github.com/pia-piyanutnithi/defect-detection-for-QA/assets/143199969/13409e9d-acc8-47a3-9fb7-e8ff6fcb734f)

### Stage 2: Multiclass Classification - "What kind of defect is this?"

The second stage delves deeper, utilizing a multiclass classification model to categorize different types of defects. This granular information helps pinpoint root causes and optimize production processes based on the prevalent defect types. For example, a high frequency of "head-scratch" defects might indicate problems with the mold or machinery in that specific area.

In the second stage, I have to be more detail on pre processing the data since it is very skewed. I used oversampling and undersampling technique to normalize the data. Then, using gridsearch and trial and error of multiple iterations(18 in total) to find the best result. 
![Capstone_Piya_Defect Detection for Quality Assurance in the Industrial Manufacturing Process (4)](https://github.com/pia-piyanutnithi/defect-detection-for-QA/assets/143199969/b54e21c0-2903-4710-b5f8-1debc7df3111)

**The Best Model Configuration**
- Pre-trained model: ResNet50 
- Activation function: Sigmoid 
- Epochs: 50 
- Learning Rate: 0.1 
- Optimizer: Adam 
- Units: 32 
- Batch Size: 16 

**The Result**
- Accuracy: 0.70
- Loss: 14.17
- Weighted Precision: 0.92
- Weighted Recall: 0.76
- Weighted F1 Score: 0.77

![Capstone_Piya_Defect Detection for Quality Assurance in the Industrial Manufacturing Process (3)](https://github.com/pia-piyanutnithi/defect-detection-for-QA/assets/143199969/d28ef386-d5f2-4b05-b05a-0ece7f4dbae7)


### Stage 3: Semantic Segmentation - "Where exactly is the defect?"

This advanced stage pinpoints the precise location of defects using a semantic segmentation model. This is particularly valuable for situations where defects are subtle or located in hard-to-reach areas, such as intricate electronic components. While object detection was initially considered, the finer granularity of semantic segmentation proved more suitable for accurately capturing the size and location of imperfections.

**The Best Model Configuration**
- Pre-trained model: UNet 
- Loss: iou 
- Optimizer: Adam  
- Epochs: 5

**The Result**
- loss: 0.5665
- accuracy: 0.7677 
- compute_iou: 0.7820

![Capstone_Piya_Defect Detection for Quality Assurance in the Industrial Manufacturing Process (5)](https://github.com/pia-piyanutnithi/defect-detection-for-QA/assets/143199969/091931fd-5798-4b63-b97b-3d5a99a9fa05)


This project lays the groundwork for a powerful defect detection system in industrial manufacturing. Future iterations will focus on incorporating real-time feedback loops, exploring advanced anomaly detection techniques, and integrating with existing production line infrastructure.

![Capstone_Piya_Defect Detection for Quality Assurance in the Industrial Manufacturing Process (6)](https://github.com/pia-piyanutnithi/defect-detection-for-QA/assets/143199969/bc4f4154-5962-4a2b-900f-ef2140e5dca6)
*Apart from manufacturing, there are many other potential industries to implement this model such as agriculture, healthcare and construction*



### Join the Conversation:

This project welcomes open collaboration and feedback! Feel free to explore the code, suggest improvements, and share your thoughts on how machine learning can revolutionize industrial quality assurance.

![Capstone_Piya_Defect Detection for Quality Assurance in the Industrial Manufacturing Process (7)](https://github.com/pia-piyanutnithi/defect-detection-for-QA/assets/143199969/1dcac2ba-1e8b-428f-9873-9a44fe2b1569)

This README represents just a glimpse into the capabilities of this project. To delve deeper, explore the code and follow the journey of innovation!
Also, feel free to add me on LinkedIn.

![Capstone_Piya_Defect Detection for Quality Assurance in the Industrial Manufacturing Process (8)](https://github.com/pia-piyanutnithi/defect-detection-for-QA/assets/143199969/c61d2cd0-14fd-4beb-b8ef-e153ed3f0c34)
*[My LinkedIn Profile Link]: (https://www.linkedin.com/in/pianithi/)*

























## Dataset
The data is a part of MVTec anamoly detection dataset from [MVTec] (https://www.mvtec.com/company/research/datasets/mvtec-ad) 
It contains good and defect images and groundtruth mark of the defect images.

## Installation
To install the requirements
run

```
virtualenv venv
source venv/bin/activate
pip install -r requirements.txt
```



