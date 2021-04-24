# Adversarial Attacks on Traffic Sign Classification

Train a CNN classifier with PyTorch for traffic sign recognition based on "model_cnn", with four convolutional layers plus one fully-connected layer in Section "Some example networks" (or you may choose to design your own architecture, or start from a pretrained network, e.g., LeNet, AlexNet or ResNet, and perform transfer learning/fine-tuning):

  1. [Chapter 3 - Adversarial examples, solving the inner maximization](https://adversarial-ml-tutorial.org/adversarial_examples/)
  [The German Traffic Sign Recognition Benchmark (GTSRB)  dataset](https://benchmark.ini.rub.de/gtsrb_news.html) (download GTSRB_Final_Training_Images.zip and GTSRB_Final_Test_Images.zip).
  Report the accuracy of your classifier on the testset.  
  (Tips: Consider converting the color images to grayscale to reduce training time. Then you only need to change the number of classes. Since model_cnn is quite small, do not expect high accuracy, and accuracy is not part of the grading criteria. The purpose of this assignment is to make you familiar with the basics, not to ask you to spend a lot of time tuning hyperparameters. )  
  2. Use your trained CNN, and start from each input image of a STOP sign that is classified correctly by your CNN, perform: (if you cannot finish Step 1 successfully, you may choose to download a pretrained PyTorch model for GTSRB from the internet and perform Step 2 based on it, but then you lose part of the points.)  
    2.1 Untargeted attack using Fast Gradient Sign Method (FGSM), using the function fgsm().  
    2.2 Untargeted attack using Projected Gradient Descent, using the function pgd_linf() (use the Projected Steepest Descent variant to accelerate the process).  
    2.3 Targeted attack using Projected Gradient Descent, using the function pgd_linf_targ(), which aims to maximize logit of the target class y_targ and minimize logit of the true class y. You may choose any target class, but I suggest using one of the "Speed Limit" signs.  
    2.4 Targeted attack using Projected Gradient Descent, using the function pgd_linf_targ2(),  which  aims to maximize logit of the target class y_targ and minimize logit of all the other classes y'.

For each attack, report the accuracy of the attacked classifier on the testset, and show visualization of a few examples of successful attack (original image and attacked image).

Put everything in one ipynb file and submit it, along with a short report in PDF containing the test accuracy and visualization of examples, as well as any problems you encountered or any insights you want to share. You may choose to embed the report within the ipynb file, execute it to show all results, then and print it as PDF, or you may write it separately. You may use either Google CoLab or your local machine. The submission deadline is tentatively set to midnight Apr 30.
