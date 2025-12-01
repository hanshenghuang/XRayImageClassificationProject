# COVID-19 Detection from Chest X-Ray Images Using AI Models

## Backgroundd
Since COVID-19 emerged, it has caused over three million deaths worldwide, making outbreak control an urgent priority for governments and public health experts. Most countries rely on testing and isolating confirmed cases to prevent large-scale transmission.  
However, RT-PCR—the standard diagnostic test—is costly, time-consuming, and requires specialized personnel. Using AI models to detect COVID-19 could provide faster, accurate results while reducing manpower needs, enabling quicker identification and isolation of infected individuals and helping prevent widespread outbreaks.

## Research Framework
Since COVID-19 primarily affects lung function, examining a person’s lung condition may help determine whether they are infected. Building on previous research, this report aims to use an AI model to analyze chest X-ray images and identify whether an individual has COVID-19.  
### 1. Preprocess
Clean and preprocess chest X-ray data, apply data augmentation, and use transfer learning techniques to address the limited dataset.
### 2. Build & Classify
Develop multiple classification models—including Logistic Regression, SVM, MLP, CNN, and VGG—to determine whether an individual is infected with COVID-19 based on chest X-ray images.
### 3. Interpret
Apply LIME to interpret model predictions and highlight important regions of the X-ray images, providing medical professionals with insights into the model’s decision-making process.

## Data Source
[Kaggle Covid-19 Image Dataset](https://www.kaggle.com/pranavraikokte/covid19-image-dataset) 
Sample Data:  
![image](https://github.com/hanshenghuang/XRayImageClassificationProject/blob/main/XRay_Sample.png)  

## Outcome 
Detailed Report: [COVID-19 Detection from Chest X-Ray Images Using AI Models](https://github.com/hanshenghuang/XRayImageClassificationProject/blob/main/covid19_detection_from_chest_xray_images_using_ai_models.pdf)

<table>
   <tr>
      <td></td>
      <td></td>
      <td>Logistic Regression</td>
      <td>SVM</td>
      <td>MLP</td>
      <td>CNN</td>
      <td>VGG</td>
   </tr>
   <tr>
      <td>Original Dataset</td>
      <td>Accuracy</td>
      <td>84.80%</td>
      <td>86.40%</td>
      <td>81.80%</td>
      <td>89.40%</td>
      <td>92%</td>
   </tr>
   <tr>
      <td></td>
      <td>Precision</td>
      <td>84.90%</td>
      <td>86.00%</td>
      <td>84.10%</td>
      <td>90.30%</td>
      <td>94%</td>
   </tr>
   <tr>
      <td></td>
      <td>Recall</td>
      <td>83.70%</td>
      <td>86.20%</td>
      <td>81.50%</td>
      <td>89.50%</td>
      <td>92%</td>
   </tr>
   <tr>
      <td></td>
      <td>F1-score</td>
      <td>0.83</td>
      <td>0.86</td>
      <td>0.81</td>
      <td>0.89</td>
      <td>0.92</td>
   </tr>
   <tr>
      <td>Balanced Dataset (111)</td>
      <td>Accuracy</td>
      <td>78.80%</td>
      <td>90.90%</td>
      <td>75.70%</td>
      <td>92.80%</td>
      <td>91%</td>
   </tr>
   <tr>
      <td></td>
      <td>Precision</td>
      <td>78.20%</td>
      <td>91.20%</td>
      <td>63.90%</td>
      <td>88.40%</td>
      <td>93%</td>
   </tr>
   <tr>
      <td></td>
      <td>Recall</td>
      <td>77.80%</td>
      <td>90.80%</td>
      <td>63.20%</td>
      <td>86.50%</td>
      <td>91%</td>
   </tr>
   <tr>
      <td></td>
      <td>F1-score</td>
      <td>0.78</td>
      <td>0.91</td>
      <td>0.58</td>
      <td>0.86</td>
      <td>0.91</td>
   </tr>
   <tr>
      <td>Balanced Dataset (500)</td>
      <td>Accuracy</td>
      <td>84.80%</td>
      <td>94.00%</td>
      <td>83.30%</td>
      <td>93.90%</td>
      <td>98%</td>
   </tr>
   <tr>
      <td></td>
      <td>Precision</td>
      <td>84.30%</td>
      <td>94.40%</td>
      <td>85.60%</td>
      <td>93.70%</td>
      <td>99%</td>
   </tr>
   <tr>
      <td></td>
      <td>Recall</td>
      <td>84.10%</td>
      <td>94.10%</td>
      <td>83.20%</td>
      <td>93.30%</td>
      <td>98%</td>
   </tr>
   <tr>
      <td></td>
      <td>F1-score</td>
      <td>0.84</td>
      <td>0.94</td>
      <td>0.83</td>
      <td>0.93</td>
      <td>0.98</td>
   </tr>
   <tr>
      <td>ZCA (80x80)</td>
      <td>Accuracy</td>
      <td>77.30%</td>
      <td>70.00%</td>
      <td>65.10%</td>
      <td>68.20%</td>
      <td>89%</td>
   </tr>
   <tr>
      <td></td>
      <td>Precision</td>
      <td>76.50%</td>
      <td>70.20%</td>
      <td>65.20%</td>
      <td>68.60%</td>
      <td>92%</td>
   </tr>
   <tr>
      <td></td>
      <td>Recall</td>
      <td>76.50%</td>
      <td>69.40%</td>
      <td>64.40%</td>
      <td>67.30%</td>
      <td>89%</td>
   </tr>
   <tr>
      <td></td>
      <td>F1-score</td>
      <td>0.76</td>
      <td>0.69</td>
      <td>0.65</td>
      <td>0.67</td>
      <td>0.89</td>
   </tr>
</table>

## Conclusion
* Using our trained VGG model, we can predict infection status with high accuracy and identify which specific lung regions are most important to the model, thereby improving its credibility.
* By increasing the number of images through rotation, scaling, and other augmentation techniques, we effectively enhance model accuracy.
* The COVID-19 cases in the dataset may mostly consist of patients with severe symptoms, which is why abnormalities in the lungs appear more pronounced.
* Machine learning requires large datasets for effective training and validation. Collecting more clinical data in the future would further improve the model’s accuracy and reliability.
* Through explainable AI, we observed that areas near the heart and spine in X-ray images are particularly important. Understanding these key regions increases model trustworthiness and may assist medical professionals in diagnosis and treatment.
