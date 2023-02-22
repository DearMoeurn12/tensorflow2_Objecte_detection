# Training Custom Object Detector

### Create TensorFlow Records
TensorFlow\workspace\training_demo\scripts\preprocessing>
for train: 
```
python generate_tfrecord.py -x C:/Users/AINext-Gen/TensorFlow/workspace/training_demo/images/train -l C:/Users/AINext-Gen/TensorFlow/workspace/training_demo/annotations/label_map.pbtxt -o C:/Users/AINext-Gen/TensorFlow/workspace/training_demo/images/train.record
```
for test: 
```
python generate_tfrecord.py -x C:/Users/AINext-Gen/TensorFlow/workspace/training_demo/images/test -l C:/Users/AINext-Gen/TensorFlow/workspace/training_demo/annotations/label_map.pbtxt -o C:/Users/AINext-Gen/TensorFlow/workspace/training_demo/images/test.record
```


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
