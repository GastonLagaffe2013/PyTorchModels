# PyTorchModels
An attempt to have one code file to test and compare multiple neural networks. Currently, the ist of Networks implemented is:
  - ResNeXt50
  - ResNet18
  - ResNet34
  - ResNet50
  - ResNet101
  - ResNet152
  - AlexNet
  - SqueezeNet
  - Vgg11
  - Vgg13
  - Vgg16
  - Vgg19
  - DenseNet121
  - DenseNet161
  - DenseNet169
  - DenseNet201

The code expects an ini file to define the location of the data and the classification information. The suffix is used to distinguish the snapshots. The default ini file is using these values:
```
[CheckPoint]
suffix = Grade.pth

[Data]
home = grade/
ipath = /
ClassNames = ["G-0","G-1","G-2","G-3","G-4"]
```
## Command Line Parameter
The code has some command line parameters to drive the run:
- s: show a first batch of images so you can check your net is seeing the right data
- t: run the training
- v: verify the trained network
- b: batch size
- l: batch limit (usually all images are processed in one epoch, with -l 10 you can limit the number of batches)
- e: number of epochs
- i: start with a clean network without using snapshots
- np: load the network without the pre-trained wieghts
- ts: percentage of data to use for testing the net (10 = 10%)
- n: name of the network to test, use list to get a list
- c: name of a config file to switch ebtween data sets

## Sample Data
In the dubdirectoy grade, there is a smaple data set with pictures of diffent print grades (g0-g4) taken with a microscope and the matching classification and validation in the csv files. 
