According the paper titled "Land-Cover Classification with High-Resolution Remote Sensing Images Using Transferable Deep Models":
Using GID public dataset, we can summerize the following points:

1- The size of the 150 4-bands training images are the same "7200x6800".
2- The large-scale classification includes 5 classes: 
(Built-up: Red, Farm-land: Green, Forest: Cyan, Meadow: Yellow, and Water: Blue).
3- They trained deep learning model using patches with multiple scales to exploit the multi-scale contextual information:
(patches of size: 65x65, 112x112, 224x224) randomly sampled on each training image.
4- If 80% pixels in a patch are covered by the same category, this patch is considered as a training sample.
5- For each 5 categories, 10000 samples are selected for each scale. Thus, a total of 10000x3x5=150000 patches are collected.
6- Then these patches are uniformly resized to 224x224 to pre-train ResNet-50 model.
7- The parameteres of ResNet-50 initialized with ImageNet. While, the softmax layer is initialized by Gaussian distribution.


