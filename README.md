# Hyperparameter Hackers
Creating a GAN model from scratch that can generate images of dogs, cats, horses, elephants, and lions. Best working model is with the Wasserstein loss function with gradient penalty. 

## Runnable Scripts and Commands:
### To evaluate the trained models for all datasets, under the directory "model", run the 'evalute_model.ipynb' in Google Colab 
### To retrain the models, under the directory "model", edit/run the 'GAN_model.ipynb' in Google Colab

## Contributions:

### Ike Pawsat:
- Responsible for: data collection, data preprocessing, hyperparameter search, model training and evaluation, paper write up, and CIFAR-10 results with data upsizing.
### Katie Baek:
- Added the data pipeline, infrastructure to easily save working models and images, FID and KID metrics, Wasserstein loss function, W-GAN with gradient penalty, and notebook to recreate results
### Kayla Imbriale:
- [...]
### Riley Byrnes:
- Original GAN model work before final improvements, one-hot vector encoding trial / attempt
