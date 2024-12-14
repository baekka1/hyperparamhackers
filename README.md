# Hyperparameter Hackers
Creating a GAN model from scratch that can generate images of dogs, cats, horses, elephants, and lions. Best working model is with the Wasserstein loss function with gradient penalty. 

## Runnable Scripts and Commands:
To evaluate the trained models for all datasets, under the directory "model", run `evalute_model.ipynb` in Google Colab

To retrain the models, under the directory "model", edit/run `GAN_model.ipynb` in Google Colab

## Contributions:

### Ike Pawsat:
- Responsible for: data collection, data preprocessing, hyperparameter search, model training and evaluation, paper write up, and CIFAR-10 results with data upsizing.
### Katie Baek:
- Added the data pipeline, infrastructure to easily save working models and images, and FID and KID metrics in `GAN_model.ipynb`, Wasserstein loss function in `W_GAN_model_FAILED.ipynb`, W-GAN with gradient penalty in `W_GAN_with_GP.ipynb`, and `evaluate_model.ipynb`
### Kayla Imbriale:
- [...]
### Riley Byrnes:
- Original GAN model work before final improvements, one-hot vector encoding trial / attempt
