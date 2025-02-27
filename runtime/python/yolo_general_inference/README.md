This is a general YOLO architecture Hailo inference example.  

The example takes one or more images, performs inference using the input HEF file and draws the detection boxes, claas type and confidence on the resized image.  
The example works with .jpg, .jpeg, .png and .bmp image files.  

The example was tested with the following Hailo Models Zoo networks:  
yolov3, yolov3_gluon, yolov4_leaky, yolov5s, yolov5m_wo_spp, yolox_l_leaky, yolov6n, yolov7, yolov7_tiny, yolov8m

## Prerequesities:  
numpy  
zenlog  
Pillow  
hailo_platform >= 4.14.0 (installed from the HailoRT .whl, tested on version 4.14.0)  
Hailo Model Zoo prerequesities (tested on version 2.8.0)

Install the hailo model-zoo, and hailort whl, and then the requirements:
`pip install -r requiremets.txt`


## Running the example:  
```./yolo_inference.py HEF.hef PATH_TO_IMAGES_FOLDER_OR_IMAGE YOLO_ARCH [--class-num NUM_OF_CLASSES] [--labels LABELS_PATH]```

You can download a sample image and a HEF with the `get_sources.sh` script, and then execute the inference.
for example:  
```CUDA_VISIBLE_DEVICES=9 ./yolo_inference.py ./yolov7.hef ./zidane.jpg yolo_v7```

For more information, run ```./yolo_inference.py --help```   
