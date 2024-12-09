# hyperparamhackers
Enhancing GAN models to create images of dogs, elephants, and other animals.
Hyperparameter Hackers Milestone Progress Report
Our final project involves using, and improving upon a DC-GAN to generate images of various animals, while adding functionality to choose the animal that the model will generate. In addition, time allowing, we will add enhancements to a traditional GAN to see if we can get better results without adding the convolutions. 

Literature Review 
Unsupervised Representation Learning with Deep Convolutional Generative Adversarial Networks: This paper proposes an improvement upon the traditional GAN by getting rid of the fully-connected linear layers and using deep convolutional layers instead (DC-GAN). It also uses batch-norm in both the generator and discriminator and instead of pooling in-between layers, it uses strided convolutions. It keeps the ReLU activation function in all generator layers except for the output, which uses the TanH function. In the discriminator, they use the LeakyReLU function. 
Image Augmentations for GAN Training: This paper considers whether adding image augmentations during the GAN training process makes significant model improvement. Previously, adding image augmentation was not desirable since the discriminator would learn the augmentations as part of the image distribution and guide the generator accordingly. They found that only adding the augmentations for the generator did not have any impact, where adding the augmentations for both the generator and discriminator did result in a significant improvement.  
An Improved GAN using Distance Restraints: 
Simple Yet Effective Way of Improving the Performance of GAN: 
Data Pipeline
Data Source: https://www.kaggle.com/datasets/antobenedetti/animals 
Above is the kaggle dataset that the project utilizes, it has fifteen thousand photos of dogs, horses, cats, lions, and elephants in total. For these preliminary results the model focused on training the model on dog photos. Our team recognized the extensive training time of GANs and from the start the project has focused on how to reduce this to make it feasible. One of the first things done to the data was size it down from 512x512 images to 128x128 images. This makes the training time faster and helps format the images for the model size. Next the data pipeline gray scales the images and by doing so reduces the “width” of the photos from three to one, further improving the training speed. Next to further conserve time, rather than processing the data each time the model is loaded, the data pipeline saves the processed images in a labeled folder, like processedlion for lions, in the user’s google drive. Additionally, in order to avoid duplicating the data, the pipeline has a purposeful error at the top that requires the user to comment it out if they really intend for the code block to run. These three steps of resizing, grayscaling, and saving to labeled folders make up the data pipeline.

Baseline Model Running


	Our model prints the loss for the generator and discriminator for each epoch and shows the loss over time in the TensorBoard (still to-do). The generator loss reflects the generator’s success in creating realistic images while the discriminator loss measures how well the discriminator distinguishes between real and fake images. Our TensorBoard also shows the development of the generated images over time, which is helpful for our training purposes to see how the model develops over time. 

Preliminary Results
	Using the model outlined in the DCGAN paper, we were able to get okay results. While none of our generated images fully look like dogs, they are very dog-like and our eyes were able to register them as dogs. [add information on the evaluation metric once we get it]. 

Next Steps
	Our next steps are to train on the other datasets and implement a way of choosing which animal we want the model to generate. In addition, we are going to add image augmentation to both the generator and discriminator in hopes of improving model performance. As shown in the paper “Image Augmentations for GAN Training”, spatial augmentations outperforms image augmentations so we are going to try doing spatial augmentations first. In addition, the paper made the augmentations to a vanilla GAN for unconditional image generation (SNDCGAN as proposed in this paper) while we will be adding the augmentations to the DC-GAN. Another thing we are going to do is try a different loss function. The loss function we are currently using is binary cross entropy and our alternative loss function uses the Wasserstein distance. This loss function uses weight clipping [add more details later…]. Our hope that this loss function will reduce the chance of mode collapse, where the model produces repetitive or limited outputs. 

**Runnable Scripts and Commands:**

**Contributions:**

**Ike Pawsat:**
**Katie Baek:**
**Kayla Imbriale:** 
**Riley Byrnes:**
