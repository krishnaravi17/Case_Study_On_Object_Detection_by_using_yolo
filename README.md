# Case_Study_On_Object_Detection_by_using_yolo

## Used YOLO
You only look once (YOLO) is a state-of-the-art, real-time object detection system.
On a Pascal Titan X it processes images at 30 FPS and has a mAP of 57.9% on COCO test-dev.

## How It Works

Prior detection systems repurpose classifiers or localizers to perform detection. They apply the model to an image at
multiple locations and scales. High scoring regions of the image are considered detections.

We use a totally different approach. We apply a single neural network to the full image. This network divides the image
into regions and predicts bounding boxes and probabilities for each region. These bounding boxes are weighted by the
predicted probabilities.

Our model has several advantages over classifier-based systems.
It looks at the whole image at test time so its predictions are informed by global context in the image.
It also makes predictions with a single network evaluation unlike systems like R-CNN which require thousands for a
single image. This makes it extremely fast, more than 1000x faster than R-CNN and 100x faster than Fast R-CNN. See
our paper for more details on the full system.
