# ColonyCounter
An android app to automatically count microbial colonies on Petri dish photos
The project is WIP, only the model in .onnx is publicly availible now. Any data or further questions will be provided or answered on request

Development details:
Base model - yolo8n.pt
Training params:
    epochs=100,
    imgsz=640,
    batch=16,
    lr0=0.0005,
    lrf=0.0005,

The model was trained on a dataset of photos from my bachelor's university microbiology lab. Dataset was supplemented via mirroring. Colonies and letters were annotated in CVAT by hand. The app differentiates between letters and colonies because the former are common on Petri dishes and can make counting challenhing

The app .apk:
https://drive.google.com/file/d/1X2sMHMBFTDZ4VPut_BTUjDtatmfTtIb_/view?usp=sharing

Here is the .yaml for dataset parametrs:

path: -
train: images/train
val: images/val
nc: 2
names: ['colony','letter']

