# PNEUMONIA DETECTION ON CHEST X-RAY IMAGES USING DEEP LEARNING

Application of Machine Learning, Deep Learning or/and Artificial Intelligence has increased tremendously in the field of medicine over the past few years. Especially if we see a sub-field of medical imaging in which we try to analyze images of X-rays, ECGs (Electrocardiogram), and other technologies to diagnose diseases or ailments in various patients.

## BUSINESS UNDERSTANDING

Pneumonia is a leading cause of death worldwide, and early detection is crucial for effective treatment. Manual interpretation of chest X-ray images by radiologists is time-consuming and prone to human error, leading to delayed diagnosis and treatment.

**Objective**: To develop a deep learning model to automate the process of pneumonia detection from chest X-ray images, enabling faster and more accurate diagnosis.

## DATA UNDERSTANDING

The dataset is organized into 3 folders (train, test, val) and contains subfolders for each image category (Pneumonia/Normal). There are 5,863 X-Ray images (JPEG) and 2 categories (Pneumonia/Normal) - labeled data

Chest X-ray images (anterior-posterior) were selected from retrospective cohorts of pediatric patients one to five years old from Guangzhou Women and Children’s Medical Center, Guangzhou. All chest X-ray imaging was performed as part of the patient’s routine clinical care.

For the analysis of chest X-ray images, all chest radiographs were initially screened for quality control by removing all low-quality or unreadable scans. The diagnoses for the images were then graded by two expert physicians before being cleared for training in the AI system.

## DATA CLEANING, EXPLORATION & VISUALIZATION

Data cleaning: Address any missing values, outliers, or inconsistencies in the dataset. Feature engineering: Extract meaningful features from the chest X-ray images that can contribute to pneumonia detection, such as texture patterns or lung region segmentation. Data transformation: Normalize or standardize the data as required for the deep learning model.

Images distribution across training, test & validation data clearly showed an imbalanced image dataset which was handled by normalization of the dataset.

![image](https://github.com/MarvinAgumba/PHASE-4-PROJECT/assets/122484885/17ec97ca-f620-4753-ba31-f8d0c45a5656)

Xray images show differences in Pneumonic Images (Existence of Opaquenes) & Normal (Clear Xray Images)

### Pneumonic Images
![image](https://github.com/MarvinAgumba/PHASE-4-PROJECT/assets/122484885/0656d8a5-eb69-49c1-94c3-dffbebffdc30)

### Normal Images
![image](https://github.com/MarvinAgumba/PHASE-4-PROJECT/assets/122484885/92291e6f-00ed-440f-a970-627c66db0c12)

### Checking illumination effects on images
![image](https://github.com/MarvinAgumba/PHASE-4-PROJECT/assets/122484885/49a5a4f6-46be-4018-a3c2-9da66df6f21f) ![image](https://github.com/MarvinAgumba/PHASE-4-PROJECT/assets/122484885/374c99f0-ed55-4bcf-9912-1c6e21e3d7a9)

In the above visualization, it is clear that illumination effects possess differences. We shall normalize the images using grayscale normalization to reduce the effects of illuminations.

CNN does not take care of images with different rotations, scales, or with different properties.

## MODELLING & EVALUATION

**Model selection**: CNN model with 4 hidden layers returning an accuracy score of **88%**

Visualizing the loss & accuracy curves clearly shows the training accuracy increases as we increase epochs while validation accuracy is irregular due to data variations.
Training loss remains relatively low & constant which is a good story

![image](https://github.com/MarvinAgumba/PHASE-4-PROJECT/assets/122484885/50f7df25-85e8-4ef6-bc13-51ce29d3c8c0)

Confusion matrix for the selected model

![image](https://github.com/MarvinAgumba/PHASE-4-PROJECT/assets/122484885/2072691f-a0df-425c-a4c5-105602f2da1b)

## RECOMMENDATION & CONCLUSSION

- This model can be used in the Healthcare sector in the radiological department to assist predict chest xray images easily and accurately. A similar model likewise can be improved on and deployed to assist with the detection of any infectious lung diseases.

- Further, tune the model (adding epochs, acquiring more data) to improve accuracy & reducing runtime. This shall help improve efficiency

- 




