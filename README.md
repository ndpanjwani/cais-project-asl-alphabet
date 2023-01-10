# CAIS++ Winter Project: ASL Alphabet

Naina Panjwani, npanjwan@usc.edu 
For my project, I chose to train a machine learning algorithm that can classify and differentiate between American Sign Language letters. I used a Kaggle dataset (ASL Alphabet Version 1 by Akash Nagaraj) that contained 87,000 200 x 200 pixel images with 29 classes. Of the 29 classes, 26 are for the letters A-Z and the 3 rest of the classes are for SPACE, DELETE and NOTHING. However, when I ran the model with all 87,000 images, the training time was too long and my Kaggle notebook grew inactive. So, I only processed every other image (43,500 images) to decrease the training time.  

I decided to use transfer learning on a pre-trained computer vision model (ResNet-50) to train the algorithm and classify the 29 classes. The hyperparameters I settled on were the model itself, the criterion, the optimizer, the scheduler, and the number of epochs. These are a good set for my specific task because the Adam optimizer and the criterion (loss function) are used in forward pass and back propagation while the scheduler sets the learning rate.  

I chose to evaluate my model based on the average of the batch losses. By calculating the running loss divided by the size of the dataset, I found the estimate of the ‘epoch loss’ during the training process so I can see how well the model is being trained. My overall loss was about 0.1421 and the loss per step ran was about 0.011 so the model trained relatively well.

My dataset, model architecture, and training procedures fit the task at hand however I think it could be better to test it on more images as sometimes when I run my model it stops at the first couple thousand images. If I was able to run all 87,000 images, I probably would have received better, more accurate results. For the metrics, I feel like I should have found the training and testing loss for more accuracy as I only focused on the training loss. 
I believe my efforts can be extended to wider implications in education and everyday life. There are many barriers in learning for deaf people due to language constraints and models like these can bridge this gap to allow deaf or hard of hearing people to communicate more easily with their peers and vice versa. 

If I were to continue this project, my next steps would be to increase the training dataset so the model can deliver accurate and proper results.


Nagaraj, A. (2018). ASL Alphabet, Version 1. Retrieved January 4, 2023 from https://www.kaggle.com/datasets/grassknoted/asl-alphabet.

