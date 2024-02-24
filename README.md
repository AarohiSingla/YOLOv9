# YOLOv9 on custom dataset:

#### Check this video for the understanding of code: https://youtu.be/3iLJ6YWPg28

![download](https://github.com/AarohiSingla/YOLOv9/assets/60029146/4648e5d6-6b6e-4e88-9f22-7fb0b599dd04)


### Environment setup:

git clone https://github.com/WongKinYiu/yolov9.git

cd yolov9

pip install -r requirements.txt

#### Train model - 
!python train_dual.py --workers 8 --batch 4  --img 640 --epochs 50 --data /mydrive/yolov9/yolov9/data.yaml --weights /mydrive/yolov9/yolov9-e.pt --device 0 --cfg /mydrive/yolov9/yolov9/models/detect/yolov9_custom.yaml --hyp /mydrive/yolov9/yolov9/data/hyps/hyp.scratch-high.yaml

#### Detections using custom trained model:
!python detect.py --img 1280 --conf 0.1 --device 0 --weights /mydrive/yolov9/yolov9/runs/train/exp9/weights/best.pt --source /mydrive/yolov9/furniture.jpg

