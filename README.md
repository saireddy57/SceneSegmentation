# Scene Segmentation with UNET Using Knowledge Distillation

This project implements a UNET-based semantic segmentation model for road scene segmentation. We utilized knowledge distillation to enhance the training process by transferring knowledge from a larger teacher model (Resnet34 backbone) to a smaller student model (Resnet18 backbone). The objective was to maintain high accuracy while reducing the model size for efficient deployment.

## Model Architecture:

Teacher Model: UNET with Resnet34 backbone
Student Model: UNET with Resnet18 backbone
Knowledge Distillation: Online distillation, where both models are trained simultaneously and the student model learns from the teacher’s feature maps and predictions.

## Dataset:
This dataset provides data images and labeled semantic segmentations captured via CARLA self-driving car simulator. The data was generated as part of the Lyft Udacity Challenge . This dataset can be used to train ML algorithms to identify semantic segmentation of cars, roads etc in an image.

## Knowledge Distillation Approach:
We applied online knowledge distillation, where both the teacher and student models are trained in parallel. The student model receives two types of guidance:

Distillation Loss: Leveraging the softer output of the teacher model to guide the student, helping it learn intermediate features that improve its generalization.

## Training Results:

Train Loss: 0.157

Train IOU: 0.650

Validation Loss: 0.210

Validation IOU: 0.623

The model achieves a good balance between accuracy and computational efficiency, with the student model reaching a **Train IOU of 0.650 and a Validation IOU of 0.623**.

Future Improvements:
Fine-tuning hyperparameters to improve generalization.
Experimenting with other teacher-student combinations or backbone architectures.
Exploring post-processing techniques to enhance segmentation accuracy.

### Metrics

<img src="https://github.com/user-attachments/assets/dfc9883e-315b-44bc-a1e3-882e80f7b2ed" alt="My Image" width="400"> <img src="https://github.com/user-attachments/assets/82c26072-3113-41aa-aefd-172081ff93a2" alt="My Image" width="400">

<img src="https://github.com/user-attachments/assets/1aa6df8c-67ff-4fc6-92d0-495e7e3a3022" alt="My Image" width="400"> <img src="https://github.com/user-attachments/assets/fd9bd615-1e93-4c9c-9d39-97c71cbd34f0" alt="My Image" width="400">
