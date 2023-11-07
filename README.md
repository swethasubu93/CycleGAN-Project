# CycleGAN for Image-to-Image Translation

### Overview
This project implements CycleGAN, a powerful deep learning model for image-to-image translation tasks. CycleGAN can be used to convert images from one domain to another, such as turning photos into artworks, converting black-and-white images to color, and much more. It offers a wide range of applications in the field of computer vision and image processing.

### Model Architecture
Our CycleGAN model consists of two generator networks (Generator A and Generator B) and two discriminator networks (Discriminator A and Discriminator B). These networks work together to learn a mapping between images from domain A to domain B and vice versa. 
The following are componenets of Cycle GAN:
- *Generators A & B*: Generator A is responsible for mapping images from domain A to domain B, while Generator B performs the reverse transformation, mapping images from domain B to domain A. The generators employ a U-Net-like architecture with skip connections to maintain image structure
- *Discriminators A & B*: Discriminator A is used to distinguish between real images from domain A and generated images from domain A (Discriminator B - vice versa for domain B). The discriminators utilize a PatchGAN approach to provide high-resolution feedback.
- *Cycle Consistency Loss*: To ensure the translated images can be accurately reversed, a cycle consistency loss is employed. It enforces that an image translated from domain A to B and back to domain A should be similar to the original image from domain A, and vice versa for domain B.
- *Adversarial Loss*: Adversarial loss, also known as GAN loss, is used to train the generators and discriminators. It encourages the generators to generate realistic images while pushing the discriminators to correctly classify real and generated images.

![CycleGAN drawio](https://github.com/swethasubu93/CycleGAN-Project/assets/109064336/657532d6-1ecf-4e0b-a709-9cdeef215d07)


### Training process
To train the CycleGAN model, we need paired datasets from the source (domain A) and target (domain B). During training, the generators aim to minimize the difference between the generated images and real images in both domains, while the discriminators attempt to distinguish between real and generated images. Training typically involves a substantial number of epochs to achieve desirable results. 

### Results
Our CycleGAN project has been successfully applied to an image-to-image translation tasks, with outstanding results. Below are some sample results showcasing the transformation of an apples to oranges and vice versa. 

- Apples to Oranges

![Apples2Oranges](https://github.com/swethasubu93/CycleGAN-Project/assets/109064336/ff003b2e-09a9-4197-a87f-ab4c4d83b5b6)
  
- Oranges to Apple

![Oranges2Apples](https://github.com/swethasubu93/CycleGAN-Project/assets/109064336/dbfd624c-e765-43e9-9723-0db86016c42d)
