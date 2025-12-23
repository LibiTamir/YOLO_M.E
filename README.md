## YOLO_M.E: BSF Mating Event Detector

YOLO-based detection of mating-related events in Black Soldier Fly (Hermetia illucens) cage recordings

This repository provides a trained YOLO object detection model for identifying mating-related events in video recordings of black soldier fly cages.
The model is intended for inference and demonstration purposes and can be applied directly to video files & images.

## Demo

# Original video
[Input video](demo/input_vid.mp4)

# Model output (annotated)
[Annotated output video](demo/output_vid.avi)

## Model overview

Architecture: YOLO (Ultralytics)

Task: Object detection

Species: Black soldier fly (Hermetia illucens)

Application: Detection of mating-related events in cage recordings

Input:

Video files (MP4 recommended)

Still images (JPG, PNG)

Output:

Annotated video or image with detected events

## Download model weights

The trained model weights (`best.pt`, ~109 MB) are provided via **GitHub Releases**.

### Steps
1. Go to the **Releases** section of this repository
2. Download `best.pt`
3. Place the file in: weights/best.pt

## Installation

This project relies on the Ultralytics YOLO framework.

Install dependencies
pip install ultralytics opencv-python

Note: PyTorch will be installed automatically by Ultralytics if not already present.
GPU acceleration is optional but recommended for faster inference.

Running inference
Inference on a video
yolo predict model=weights/best.pt source=demo/input.mp4 conf=0.25 save=True

Inference on a single image
yolo predict model=weights/best.pt source=path/to/image.jpg conf=0.25 save=True

Inference on a folder of images
yolo predict model=weights/best.pt source=path/to/image_folder conf=0.25 save=True


The annotated outputs will be saved automatically by Ultralytics.

Repository structure
bsf-mating-yolo/
├── README.md
├── weights/
│   └── best.pt        # downloaded from Releases
├── demo/
│   ├── input.mp4
│   └── output_annotated.mp4
├── scripts/
│   └── README.md

## Notes

Recommended confidence threshold: 0.8

Detection performance depends on image/video quality, lighting conditions, and cage density

The model was trained and evaluated under controlled experimental conditions

## Citation

If you use this model in academic work, please cite the associated thesis:

Tamir, L. (2025). *Computer vision and the Black Soldier Fly: behavioral tracking for reproductive success*. Master’s thesis.

Contact

For questions or inquiries, please contact:

Libi Tamir 
Department of Entomology
The Hebrew University of Jerusalem

libi.tamir@mail.huji.ac.il


