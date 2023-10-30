# RAC-UNET
My III year B.Sc project in Deep Learning

During the final semester of my B.Sc Mathematics programme, I decided to do a project as a course requirement.

This work was presented at the `NCVPRIPG 2023` conference held at `IIT Jodhpur` as part of the
`Student Research Symposium`.

# Abstract
Face masks have emerged as a quintessential accessory during the outbreak of a pandemic, especially during one that matches the scale of COVID 19. This poses a significant challenge of recreating the faces of people as the security systems we have established in our society depends heavily on methods like facial recognition etc. 
While extensive research has been conducted in the realm of facial in-painting and reconstruction employing Deep Neural Networks, the task of unmasking faces while focusing on the subtle features like that of occluded emotions, remains an under-attempted challenge.

We introduce a custom model, the `RAC-UNET (Residual Attention Conditional UNET)`, which uses emotion labels as a conditioning factors for the generation of unmasked facial images. 
The model also utilizes `Attention Gating` mechanisms and `Residual connections`. The model was trained from scratch on the `RAFDB` (Real World Affective Faces Database) with digitally imposed face masks, which was later augmented with sample from the `AFFECTNET` database. 

The training was done on P100 GPUs provided by Kaggle for 300 epochs using different loss functions. The model is also compared with a similar model that does not use an emotional label as additional input, using metrics like `MS-SSIM`, `PSNR`, `VGG-Perceptual Loss` and `Brisque score`. To verify the ability to correctly predict emotions, a `RESNET-18 based Facial Emotion Recognition model` was used with the original emotion labels as the ground truth.



# Model Architecture
![RAC-UNET](https://github.com/YeduKrishnaP/RAC-UNET/assets/98282751/16998e84-eace-410e-9f5a-7724287aaee4)

### Upscale Block
![Upscale resized](https://github.com/YeduKrishnaP/RAC-UNET/assets/98282751/d8e835e9-9066-4eab-b3ec-dd4a1df94f77)


### Downscale Block
![Downscale resized](https://github.com/YeduKrishnaP/RAC-UNET/assets/98282751/73149aff-2dc8-440e-90f2-f2dc336ea42e)


# Results and Comparison table

## Final Outputs (MS-SSIM on RAFDB + AFFECTNET for 200 epochs)
![NCVPRIPG 2023 final](https://github.com/YeduKrishnaP/RAC-UNET/assets/98282751/1e7921fd-73a4-43cd-882c-b20e760ae458)


## Outputs of model trained only on RAFDB
![4](https://user-images.githubusercontent.com/98282751/235886205-c50eab7d-d4ad-4958-9f17-d3edbedf7f0a.png)
![5](https://user-images.githubusercontent.com/98282751/235889576-15a0537b-2164-4f90-99d3-80eab3523b87.png)
![6](https://user-images.githubusercontent.com/98282751/235886214-3e4c6823-a835-490a-b516-e1f559c77d93.png)
![8](https://user-images.githubusercontent.com/98282751/235886222-2fdf6d59-97a9-4ddf-bcc2-d13f7c99467c.png)

Comparison of the models (Old, to be updated)
![Comparison table](https://user-images.githubusercontent.com/98282751/235886455-bef380da-73ba-44e5-9feb-ec4227b0f64d.png)

# Report
[Report.pdf](https://github.com/YkingAwesome/RAC-UNET/files/11381387/Report.pdf)
