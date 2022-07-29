![image](https://user-images.githubusercontent.com/91864024/181678758-1a52aef5-247d-43b6-99fd-fdfb7bfbe21c.png)
# KDD Cup Classification using ANN
## I. Outline
- A network intrusion refers to any unauthorized activity on a digital network. 
- Network intrusions often involve stealing valuable network resources and almost always jeopardize the security of networks and/or their data.
- In this project, we aim to build a model that can classify normal/ abnormal connection.
## II. Business Objective/ Problem
- Assume that you work in the Data Science department of a company that provides telecommunications services. Your task is to detect "bad" connections among everyday connections.
- Your client is suspected of having "bad" connections that could steal user information. They ask you to build a model to help them detect "bad" connections to promptly prevent and avoid loss of user data.
- This project is made based on that requirement.
## III. Project implementation
### 1. Business Understanding
Based on the above description => identify the problem:
- Find methods to classify "bad" connection among normal connections.
- Objectives/problems: build a classification model to classify these 2 connection types.
- Applied method: ANN model
### 2. Data Understanding/ Acquire
- Data is downloaded from https://archive.ics.uci.edu/ml/datasets/KDD+Cup+1999+Data
- There are 2 files to build model:
  - kddcup.data.gz: train and test your model by data in this file
  - kddcup.testdata.unlabeled.gz: predict new value in this file

![image](https://user-images.githubusercontent.com/91864024/181681300-28236fcf-75a7-4662-8eaa-1171cafebcc2.png)
### 3. Build model
#### 3.1. Understand the dataset

![image](https://user-images.githubusercontent.com/91864024/181681905-e87b1b84-35c9-4e2f-ab25-a57a47fd3ec9.png)
![image](https://user-images.githubusercontent.com/91864024/181681976-dc1817ba-6fe8-45bb-a6d3-5bd856621ef2.png)

#### 3.2. Data pre-processing
**-Check NaN, Null, duplciate:**

![image](https://user-images.githubusercontent.com/91864024/181682127-0c673709-8276-4174-845c-df531cfec16e.png)

![image](https://user-images.githubusercontent.com/91864024/181682144-784912c6-5042-4a5d-b41c-113fa03bcd76.png)

**- Make a new feature:**

![image](https://user-images.githubusercontent.com/91864024/181682379-94fe782c-3442-4ebd-aec5-013099070654.png)

![image](https://user-images.githubusercontent.com/91864024/181682414-b0156c18-f2c2-45de-8c95-56e479853921.png)

**- Dummies, scale dataset, split train/test:**

![image](https://user-images.githubusercontent.com/91864024/181694384-3a230667-f5ad-4eb2-b58b-727811e5518d.png)

![image](https://user-images.githubusercontent.com/91864024/181694471-cb93f351-a5e4-467f-8e1d-7b13ccd9f0df.png)

**- Build ANN model:**

![image](https://user-images.githubusercontent.com/91864024/181694604-ff009cea-df42-4215-9afe-c93122a4d206.png)

![image](https://user-images.githubusercontent.com/91864024/181694744-aec28ddd-e6e6-4115-a1f9-d1453db193b4.png)

![image](https://user-images.githubusercontent.com/91864024/181694974-181acec7-09ba-4d80-b9f9-ed7dad8b72ab.png)

![image](https://user-images.githubusercontent.com/91864024/181695010-41d51b8d-6bc7-4b2d-a012-55943236237b.png)

![image](https://user-images.githubusercontent.com/91864024/181695095-ae6603ba-a842-4357-868b-e4bc4578fbf2.png)

Comment: the loss of train and test is low. Accuracy of train and test are both high --> model predicts well, no under/overfitting

**- Accuracy score and confusion matrix:**

![image](https://user-images.githubusercontent.com/91864024/181695390-07c7d54d-56e6-402e-b675-b1cf26f63c84.png)

![image](https://user-images.githubusercontent.com/91864024/181695445-d6812580-7803-4b5f-b70a-88b1bc69d929.png)

Comment: from the confusion matrix and accuracy, the model is suitable for prediction

#### 3.3. Predict on new dataset

![image](https://user-images.githubusercontent.com/91864024/181695720-66377573-abe2-417d-991c-2901e47abdda.png)

**- Check NaN, Null, pre-processing as train/test dataset:**

![image](https://user-images.githubusercontent.com/91864024/181695905-899503de-0798-4fbb-aaf0-8a20096c5f73.png)

![image](https://user-images.githubusercontent.com/91864024/181695944-dbf4287d-18a3-4bd3-813d-8ca70dddd816.png)

![image](https://user-images.githubusercontent.com/91864024/181695976-fb972d16-6d29-4152-9563-1d2001acd217.png)

**- Make new prediction:**

![image](https://user-images.githubusercontent.com/91864024/181696167-2069c619-3785-4098-9df6-486a58ff45c0.png)

![image](https://user-images.githubusercontent.com/91864024/181696219-a3585a75-a9a9-42f8-8322-d06f9f188298.png)

![image](https://user-images.githubusercontent.com/91864024/181697148-ee4e3e7e-e1e3-415f-b11b-4e2b256fda17.png)

### 4. Conclusion
- Based on above analysis, ANN model can be used to predict "bad" connection
- This model can be used to detect network intrusions, protect a computer network from unauthorized users, including perhaps insiders.

Thank you for your experience with my project. Hope you enjoy it!














