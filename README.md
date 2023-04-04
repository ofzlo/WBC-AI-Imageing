# WBC-AI-Imageing
2023 Sookmyung W. Univ. graduation project   
Project: White Blood Cell(WBC) detection with AI   

This project aims to detect four types of white blood cells: eosinophils, lymphocytes, macrophages, and neutrophils, through object detection. Bounding boxes are drawn using OpenCV and objects are cropped from them to serve as input for a classification task performed by a model. We employed a MobileNetV2-based model trained on each cell image.

## Table of Contents
- [Background](#background)
- [Usage](#usage)
- [Section Explanation](#section-explanation)
  - [Image Preprocessing for annotating bounding-box](#image-preprocessing-for-annotating-bounding-box)
  - [Clustering](#clustering)
  - [Modeling](#modeling)
- [Contributors](#contributors)

## Background
Respiratory diseases pose a significant threat to human life, with high incidence rates in modern society. Among various respiratory disease tests, bronchoalveolar lavage fluid examination is the most fundamental, requiring discriminating and counting immunocytes on slide images, which is a labor-intensive task. Additionally, differential blood cell counts play an important role in general health checkups.

The current method for differential blood cell counts involves manual identification and counting of cells, resulting in long processing times and frequent errors due to reduced accuracy and consistency. As a result, recent research has focused on image preprocessing and deep learning-based methods for differential blood cell counts. However, previous research has limitations such as incomplete representation of immune cell features, low cell detection rates, and low classification accuracy, despite reducing processing time compared to manual methods. Therefore, this project aims to leverage image preprocessing and deep learning techniques to enhance detection performance.

## Usage
``` Image Preprocessing Section → Modeling ```

## Section Explanation
### Image Preprocessing for annotating bounding-box
bounding-box annotation result
![bounding-box annotation result](https://user-images.githubusercontent.com/90624848/229700811-53265a4c-8456-4703-958a-a2cdfb553e34.png)  

### Clustering
clustering result of test image   
In the actual project, clustering was performed on approximately 50,000 cropped cell images obtained from the original dataset.   

**``label 0``**   
<img src="https://user-images.githubusercontent.com/90624848/229707998-b98a9064-c21f-444f-ad89-44cdec44fadb.png" width="600">

**``label 1``**   
<img src="https://user-images.githubusercontent.com/90624848/229708027-f57592f6-61ac-4ac3-aba6-a361b2dac79e.png" width="600">

**``label 2``**   
<img src="https://user-images.githubusercontent.com/90624848/229709790-f169abb0-59ff-444f-83a1-14b83192bdfd.png" width="600">

**``label 3``**   
<img src="https://user-images.githubusercontent.com/90624848/229708014-90bad6fd-24a3-48cd-b6b2-b6ccfad87897.png" width="600">

**``label 4``**   
<img src="https://user-images.githubusercontent.com/90624848/229708005-2ebe713a-1714-444a-ab98-66eec870d270.png" width="600">

**``label 0``**      
<img src="https://user-images.githubusercontent.com/90624848/229709151-7b1aabf5-7bb0-4b7e-8cf8-f25e662de856.png" width="600">

### Modeling
The final model used was 'MobileNetV2'. During the model selection process, LeNet-5 and VGG16 were also considered. The input image was reshaped to '96x96x3'.   
####    
<img src="https://user-images.githubusercontent.com/90624848/229708787-093aecb5-7e96-4b89-a0ca-fade29c4e6da.png" width="800">

## Contributors
|[기지원](https://github.com/carlyle1233)|[조유림](https://github.com/ofzlo)|[윤혜경](https://github.com/hyetae)|
|---|---|---|
|<img src="https://media.discordapp.net/attachments/1020722484460392590/1092691846666395719/image.png" width="200">|<img src="https://media.discordapp.net/attachments/1020722484460392590/1092691846880309288/image.png" width="200">|<img src="https://media.discordapp.net/attachments/1020722484460392590/1092691846473449503/image.png" width="200">|
