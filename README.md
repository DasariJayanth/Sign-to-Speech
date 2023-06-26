# Sign-to-Speech
  
Sign-to-Speech is done in two steps.  
1. Sign-to-Text.  
2. Text-to-Speech.  
  
For the first part, ***American Sign Language(ASL)***, most commonly used sign language is used. Two types of ASL Datasets are used.  
***Dataset-1*** : ASL Dataset without bounding boxes.  
***Dataset-2*** : ASL Dataset with bounding boxes.  
  
Trained various SOTA models, custom CNN models on the both datasets and compared their results.  
  
## Dataset-1: *ASL without Bounding Boxes*  
  
| Model | Training Accuracy | Validation Accuracy | Training Time(in sec)|
|---|---|---|---|
[MobileNet](https://github.com/DasariJayanth/Sign-to-Speech/blob/1674ebdb8c9488897ca33a885ea309bfb21b54d8/models/Dataset-1/mobilenet.h5) | 65.31% | 65.91% | 1345.8388
EfficientNetB7 | 62.48% | 63.30% | 2030.4323
DenseNet201 | 58.94% | 61.17% | 1537.5592
ResNet101v2 | 61.95% | 60.31% | 1591.4062
ResNet50v2 | 61.22% | 59.86% | 1407.8828
ResNet50 | 59.06% | 58.29% | 1432.4340
VGG16 | 51.79% | 55.22% | 1584.7626
VGG19 | 51.21% | 53.21% | 1555.2616  
MobileNetV2 | 54.88% | 51.90% | 1287.8853
Xception | 52.37% | 49.87% | 1467.0641
InceptionV3 | 47.34% | 45.42% | 1409.6493
<!-- Custom CNN | 82.92% | 74.57% |29502.0000 -->

## Dataset-2: *ASL with Bounding Boxes*  
  
This dataset can be found at [roboflow](https://universe.roboflow.com/david-lee-d0rhs/american-sign-language-letters) website, created by David Lee.  
  
| Model | Training Accuracy |
|---|---|
YOLOv5x | 89%
Faster RCNN | 86%
[Custom CNN](https://github.com/DasariJayanth/Sign-to-Speech/blob/1674ebdb8c9488897ca33a885ea309bfb21b54d8/models/Dataset-2/Custom_CNN_ASL_aug_roboflow.h5) | 88%

  
For the second part, one of the top performing ***Sileros TTS*** models at the time has been used for the Speech Recognition from the Text, produced from above.  


For detailed explanation, please refer [FER.pdf](https://github.com/DasariJayanth/Sign-to-Speech/blob/723f5b9b311223c913bf37bda5fc77eb99887d75/FER.pdf).
