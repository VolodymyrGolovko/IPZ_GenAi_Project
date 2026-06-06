# Project description
The challenge is to develop a generative adversarial network to generate a proper training set for the an ML–based malware classifier. For our competition, you should generate malware behavior samples in the same format as the manually collected ones. You will notice that the manually collected training set, which contains a histogram representation of malware and ordinary software behavior, is unbalanced (3000 benign and 1465 malign samples) hence, the challenge is to:

- Train an ML model using the unbalanced real dataset (train.csv) and submit the classification outcome on the validation dataset (Validation.csv) as to get the current RMSE feedback as a baseline. Only RMSEs below 0.2 will be considered.
- Develop a GAN system using the available real dataset as guidance to generate synthetic samples of malware behavior.
- Retrain the ML model using the now balanced dataset (after integrating the GAN generated malware synthetic dataset in the original dataset).
- Test the model on the held-out validation set and submit the output. The final evaluation will be carried out by obtaining the GAN trained model RMSE and computing the absolute value of the difference with the baseline model's RMSE. In case of a tie on this difference values, the confusion matrix of the GAN trained model will be considered to asses the quality of malign sample generation.
