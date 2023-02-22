# Training Custom Object Detector




### Training the Model
train model with faster RCNN
```
python model_main_tf2.py --model_dir=models/my_faster_rcnn_resnet101_v1 --pipeline_config_path=models/my_faster_rcnn_resnet101_v1/pipeline.config

```
train model with SSD MobileNet
```
python model_main_tf2.py --model_dir=models/my_ssd_mobilenet --pipeline_config_path=models/my_ssd_mobilenet/pipeline.config

``` 

Monitor Training Job Progress using TensorBoard

```
tensorboard --logdir=models/my_ssd_mobilenet

```

for bugging
https://stackoverflow.com/questions/71759248/importerror-cannot-import-name-builder-from-google-protobuf-internal
