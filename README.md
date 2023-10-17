SM^3: Self-Supervised Multi-task Modeling with Multi-view 2D Images for Articulated Objects
----------
#### Codes and Datasets for  Self-Supervised Multi-task Modeling with Multi-view 2D Images for Articulated Objects

### Introduction

![Overview](./images/SM3_overview.pdf)

We've developed a state-of-the-art approach, SM3, aimed at handling articulated objects using multi-view RGB images both pre- and post-interaction. Here's a quick breakdown:

- **3D Reconstruction**: Our method uses a deformable tetrahedral grid for textured 3D reconstruction. This is achieved by computing post-rendering image losses for objects before and after their interaction.

- **Segmentation and Joint Estimation**: The tetrahedral structure aids in segmenting movable parts and optimizes joint parameters. Our unique workflows help in analyzing geometric structure differences, enabling better segmentation and estimation of rotational joints.

- **Refinement**: We introduce a patch-split technique that refines the image loss, enhancing the segmentation accuracy. The optimization process involves rendering the pre-interaction tetrahedral grid and matching it against post-interaction RGB images.

- **Dataset**: Recognizing the lack of datasets for articulated objects, we've introduced a comprehensive dataset named MMA, inspired by the PartNet mobility dataset. This dataset is multi-view, multi-modal, and multi-state, covering a wide range of articulated objects and categories.

This method and dataset are geared to meet evaluation demands and can also be used for training and testing various other techniques in this niche.
