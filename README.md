SM^3: Self-Supervised Multi-task Modeling with Multi-view 2D Images for Articulated Objects
----------
#### Codes and Datasets for  Self-Supervised Multi-task Modeling with Multi-view 2D Images for Articulated Objects will be released soon.

### Introduction

![Overview](./images/SM3_overview.pdf)

We've developed a state-of-the-art approach, SM3, aimed at handling articulated objects using multi-view RGB images both pre- and post-interaction. Here's a quick breakdown:

- **3D Reconstruction**: Our method uses a deformable tetrahedral grid for textured 3D reconstruction. This is achieved by computing post-rendering image losses for objects before and after their interaction.

- **Segmentation and Joint Estimation**: The tetrahedral structure aids in segmenting movable parts and optimizes joint parameters. Our unique workflows help in analyzing geometric structure differences, enabling better segmentation and estimation of rotational joints.

- **Refinement**: We introduce a patch-split technique that refines the image loss, enhancing the segmentation accuracy. The optimization process involves rendering the pre-interaction tetrahedral grid and matching it against post-interaction RGB images.

- **Dataset**: Recognizing the lack of datasets for articulated objects, we've introduced a comprehensive dataset named MMA, inspired by the PartNet mobility dataset. This dataset is multi-view, multi-modal, and multi-state, covering a wide range of articulated objects and categories.

This method and dataset are geared to meet evaluation demands and can also be used for training and testing various other techniques in this niche.


### Results

### Dataset

```
Multi-Modal Articulated Objects Dataset (MMA)
├── 100221_box
│    ├── Start_state
│    │    ├── RGB_Images: 640x480x3 (PNG)
│    │    ├── Object_Masks: 640x480x3 (PNG)
│    │    ├── Depth_Maps: [480, 640] (NPY)
│    │    └── Camera_Poses
│    │         ├── Pose: 4x4 (LDB)
│    │         ├── Intrinsic: 3x3
│    │         ├── FOV
│    │         └── joint_name
│    └── End_state
│         ├── ...
└── Additional_Info (or another appropriate directory name)
    ├── Start_state: State of the object before interaction.
    ├── End_state: State of the object after interaction.
    ├── RGB_Images: RGB images taken around the object in a specific state.
    ├── Object_Masks, Depth_Maps, Camera_Poses: Corresponding object masks, depth maps, and camera poses.
    ├── Pose: Camera pose matrix (LDB coordinate system).
    ├── Intrinsic: Camera intrinsic matrix.
    ├── FOV: Camera field of view.
    └── joint_name: Joint index.
```

