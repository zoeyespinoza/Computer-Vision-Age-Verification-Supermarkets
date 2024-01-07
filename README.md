# Computer-Vision-Age-Verification-Supermarkets
Age Verification System for Good Seed Supermarkets, using Computer Vision to implement store policies

## Project Description
Good Seed Supermarkets, a leading grocery chain, is launching a project focused on improving adherence to alcohol sale regulations. The main goal is to prevent the sale of alcohol to underage customers. As a Data Scientist, my role involves assessing and deploying a technological solution to effectively meet this challenge.

## Project Goals
- **Develop a Reliable Model:** Create a model with high accuracy in age estimation to minimize both false positives (wrongly denying a sale to of-age individuals) and false negatives (permitting underage sales).

- **Ensure Legal Compliance:** Align the model's performance with legal age requirements for alcohol sales, thereby upholding Good Seed's commitment to responsible retailing.

- **Enhance Customer Experience:** Implement a system that is non-intrusive and respects customer privacy, while efficiently carrying out age verification.

![Image](https://github.com/zoeyvero/Computer-Vision-Age-Verification-Supermarkets/blob/main/graphs/age_distr.png)
Example of age classification by images of people:
![Image2](https://github.com/zoeyvero/Computer-Vision-Age-Verification-Supermarkets/blob/main/graphs/sample_img_age_verification.png)
![Image2](https://github.com/zoeyvero/Computer-Vision-Age-Verification-Supermarkets/blob/main/graphs/age20.png)
![Image2](https://github.com/zoeyvero/Computer-Vision-Age-Verification-Supermarkets/blob/main/graphs/age40.png)
![Image2](https://github.com/zoeyvero/Computer-Vision-Age-Verification-Supermarkets/blob/main/graphs/age60.png)
![Image2](https://github.com/zoeyvero/Computer-Vision-Age-Verification-Supermarkets/blob/main/graphs/age80.png)


## Conclusions
**Data Handling and Preparation:**

The project effectively handled a large dataset of 7,600 images, employing efficient data loading techniques using ImageDataGenerator. Proper preprocessing and augmentation techniques were crucial in preparing the data for training, ensuring robustness and variety in the dataset.

**Model Architecture and Training:**

The use of a pre-trained model like ResNet50 as the backbone provided a strong feature extraction base, improving the model's accuracy. The addition of custom layers like Dense, Dropout, and GlobalAveragePooling2D allowed for tuning the model to the specific requirements of the task.

Training on a GPU platform ensured efficient utilization of computational resources, reducing training time significantly. 

The project then prepares a script to run on the GPU and outputs, 356/356 - 39s - loss: 23.9954 - mae: 3.6615 - val_loss: 70.2468 - val_mae: 6.0498, as its final output. 

The training loss decreases significantly from epoch 1 to epoch 20, indicating that the model is learning and improving its performance on the training data. Ideally, both the validation loss and MAE should decrease over time, indicating that the model is learning and generalizing well to new data. We see a mostly consistant pattern in the output, but the training loss continues to decrease while the validation loss starts to increase or stagnates towards the end, as this might indicate overfitting. The MAE gets below the the target of 8, and succeeds in the task. From the initial learning poit of the first epochs the model is learning rapidly from the training data, as indicated by a significant drop in training loss and MAE. The validation MAE decreases from epoch 1 to 6. However, the validation loss is somewhat  volatile, with an initial increase followed by fluctuations. Next from around epoch 7 onwards, both training and validation metrics appear to stabilize, but there are fluctuations in validation metrics. This could be due to possibly starting to overfit. In the latest epochs, 17 to 20, the training loss and MAE continue to decrease, and there is less of a consistent improvement in validation metrics.

The project demonstrates the capability of machine learning techniques in handling complex image recognition tasks. The skills and techniques used in this project are transferable to a wide range of applications in computer vision.
