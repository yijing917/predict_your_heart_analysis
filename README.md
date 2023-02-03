# predict_your_heart_analysis

:stethoscope:**About the dataset**

 This dataset contains *270 case studies* of individuals classified as either having or not having heart disease based on results from cardiac catheterizations - the gold standard in heart health assessment. Each patient is identified by 13 independent predictive variables revealing their age, sex, chest pain type, blood pressure measurements, cholesterol levels, electrocardiogram results, exercise-induced angina symptoms, and the number of vessels seen on fluoroscopy showing narrowing of their coronary arteries. 
 
 Credit to original dataset owner: Please refer to the [dataset here](https://www.kaggle.com/datasets/thedevastator/predicting-heart-disease-risk-using-clinical-var)
 
 
| Column Name             | Category     | Description                                                       |                                                                                                                                                                         |
|-------------------------|--------------|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Age                     | Numeric      | The age of the patient.                                           |                                                                                                                                                                         |
| Sex                     | Categorical  | The gender of the patient.                                        | 1= male , 0 = female                                                                                                                                                    |
| Chest Pain Type         | Categorical  | The type of chest pain experienced by the patient.                | 1= typical angina  2= atypical angina  3= non-anginal pain  4= asymptomatic                                                                                             |
| BP                      | Numeric      | The blood pressure level of the patient.                          | resting blood pressure (in mmgHg on admission to hospital)                                                                                                              |
| Cholesterol             | Numeric      | The cholesterol level of the patient.                             | serum cholesterol in mg/dl                                                                                                                                              |
| FBS over 120            | Numeric      | The fasting blood sugar test results over 120 mg/dl.              | 1= true, 0= false                                                                                                                                                       |
| EKG Results             | Categorical  | The electrocardiogram results of the patient.                     | 0= normal  1= having ST-T wave abnormality (T wave inversions and/or ST elevation or depression of 0.05mV) 2= showing probable or definite left ventricular hypertrophy |
| Max HR                  | Numeric      | The maximum heart rate levels achieved during exercise testing.   |                                                                                                                                                                         |
| Exercise angina         | Categorical  | The angina experienced during exercise testing.                   | 1= yes, 0= no                                                                                                                                                           |
| ST depression           | Numeric      | The ST depression on an Electrocardiogram.                        | ST depression induced by exercise relative to rest                                                                                                                      |
| Slope of ST             | Categorical  | The slope of ST segment electrocardiogram readings.               | (mg                                                                                                                                                                     |
| Number of vessels fluro | Numeric      | The amount vessels seen in Fluoroscopy images.                    | number of major vessels colored by fluoroscopy                                                                                                                          |
| Thallium                | Categorical  | The Thallium Stress test findings.                                | 3= normal, 6= fixed defect , 7= reversible defect                                                                                                                       |
| Heart Disease           | Categorical  | Whether or not the patient has been diagnosed with Heart Disease. | Presence/ Absent                                                                                                                                                        |


:stethoscope:**Heart disease definition**

Heart disease refers to a few types of heart conditions:

* CAD – may cause by the blockage in coronary arteries leads to decrease in blood flow to heart muscles 
* Heart Arrhythmias 
* Heart Failure (HF)
* Cardiomyopathy 
* Congenital Heart Disease

Heart disease is the leading cause of death for men and women in the United States.About 697,000 people in the US died from heart disease in 2020. Coronary artery disease, one of the most common hear disease ,killed 382,280 people in 2020. The latest heart disease and Stroke Statistics from the American Heart Association report that about 20.1 million adults aged 20 and older have CAD.


:drop_of_blood: **Risk Factor of CAD**
-	High blood pressure 
-	High blood cholesterol (LDL)
-	Diabetes 
-	Age 
-	Tobacco use 
-	Obesity/ overweight 
-	Excessive alcohol use 
-	Physical inactivity 


:chart_with_upwards_trend: **Diagnosis of Heart Disease** 


The general approach of diagnostic management of patient with angina and suspected CAD published by ESC 2019. Diagnostic tests are done after completing all the assessments and lifestyle/family history taking. 

![Diagnosis of heartdisease](https://user-images.githubusercontent.com/123582571/216457420-f4a43528-cf6c-4335-a2ed-00e66faee2ca.png)

***Step 1–identifying signs and symptoms***

Type of angina 
Typical angina /atypical angina/non-anginal chest pain 

Angina severity 
Stable and unstable angina 

***Step 2-Assess patient’s comorbidities and other cause symptoms***

***Step 3-Basic testing***

The first line of tests will include biochemical testing (blood test), a resting ECG, a resting echocardiography, and for some patients, a chest X-ray.

:pushpin:**Echocardiography** ( known as echo) -is a type of ultrasound which provide information about cardiac function and anatomy. 

:pushpin:**Electrocardiogram ECG**– records the electric activity of the heart to detect the abnormalities mainly in ST-segment depression. 

:pushpin:**Stress test** (also known as exercise ECG) – monitor heart when the patient is on a treadmill. 

:pushpin:**Invasive coronary angiography (ICA)** –Invasive procedure that provides clear visual of coronary arterial blood flow, and is only necessary in patients with suspected CAD in cases of inconclusive non-invasive testing. 

:pushpin:**Positron Emission Tomography (PET)** – non-invasive nuclear imaging test that uses radionuclides to create image of heart. This could be used to detect area of low blood flow in heart or dead/injured tissues. PET also used to find out if patients will be benefit from percutaneous coronary intervention (PCI) or coronary artery bypass surgery (CABG).

:pushpin:**Single-photon emission computed tomography (SPECT)**-  non-invasive nuclear imaging test that uses radioactive tracer to identify blood flow to the heart and heart function. This could help to diagnose coronary artery disease or any stroke. 

:pushpin:**Cardiac Computed Tomography Angiography (CTA or CAT scan)** – High accuracy. Uses X-rays to take photos of heart and vessels to identify the heart disease.

:pushpin:**Thallium Stress Test** – nuclear medicine study that shows blood flow through heart muscles while patient in rest or exercising. A radioisotope (Thallium201 Chloride) is given through IV to visualize the heart. 

:drop_of_blood:**Basic ECG wave Explanation**


![Picture2](https://user-images.githubusercontent.com/123582571/216461008-0706de2f-9edf-483a-90eb-f5f63a73a4b8.png)

***P wave*** – represent atrial depolarization

***QRS wave complex*** – represent ventricular depolarization.

***ST segment (ST interval)*** – reflect the period of zero potential between ventricular depolarization and repolarization. There might be ST elevation or ST depression are one of the indicator that could associate with heart issues. 

![st_elevation_st_depression](https://user-images.githubusercontent.com/123582571/216461415-89efc967-8662-4cd9-8dde-c27c0790db5a.jpeg)



![ST-segment-depression-upsloping-downsloping-horizontal](https://user-images.githubusercontent.com/123582571/216461375-b30c02a1-32c8-44b3-95aa-56c021b5d957.png)


***T wave*** - represent ventricular repolarization

ST segment is one of the most important features to identify the trend and differentiate different condition accordingly. could become either ST elevation or ST depression which might indicates there is certain abnormalities in the heart.  

![Differential Diagnosis](https://user-images.githubusercontent.com/123582571/216461695-2cbb97e1-ffac-442a-9399-2b9fb7205b00.png)

:bar_chart:**Analysis method**

 I used R to clean data and perform analysis to identify the relationship between variables and presence of heart disease.

**Findings**


![graph_1](https://user-images.githubusercontent.com/123582571/216641663-2f1343de-63fd-4b47-aecb-653112277ef1.png)


![histogram_2](https://user-images.githubusercontent.com/123582571/216641675-4fc000de-a5f7-48e8-a525-1362d2aded34.png)


![boxplot_3](https://user-images.githubusercontent.com/123582571/216641705-9688cdfe-f67f-43fc-a506-31c0179ad21a.png)


![scatterplot_4](https://user-images.githubusercontent.com/123582571/216642300-b82e7c61-1573-469b-91b3-0926a7cb2629.png)


![boxplot_5](https://user-images.githubusercontent.com/123582571/216642308-0fbb9a09-3f9f-4417-8c6e-db7e7e944384.png)


![bargraph_6](https://user-images.githubusercontent.com/123582571/216642359-4ccf1aca-57bd-4267-918c-4a0968c96e15.png)


![bargraph_7](https://user-images.githubusercontent.com/123582571/216642322-ea65356c-74a8-4885-9d58-8f3667586271.png)








