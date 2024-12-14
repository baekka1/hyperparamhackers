# Hyperparameter Hackers
Creating a GAN model from scratch that can generate images of dogs, cats, horses, elephants, and lions. Best working model is with the Wasserstein loss function with gradient penalty. 

## Runnable Scripts and Commands:
To evaluate the trained models for all datasets, under the directory "model", run `evalute_model.ipynb` in Google Colab

To retrain the models, under the directory "model", edit/run `GAN_model.ipynb` in Google Colab

## Contributions:

### Ike Pawsat:
- Added CIFAR-10 results with data upsizing in `GAN_model.ipynb`
- hyperparameter search, model training and evaluation
### Katie Baek:
- Added a data pipeline to easily download and process the data off a google drive link, model infrastructure to easily save working models and images to the Google Drive under unique names to assist with testing, calculation of FID and KID metrics, and latent space visualization in `GAN_model.ipynb`
- Coded `W_GAN_model_FAILED.ipynb`, `W_GAN_with_GP.ipynb`, and `evaluate_model.ipynb`
### Kayla Imbriale:
- Model architecture of generator and discriminator, training loop in `GAN_model.ipynb`
### Riley Byrnes:
- Original GAN model work before final improvements, one-hot vector encoding trial / attempt
