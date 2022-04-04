Caffe2
===================

Caffe2 is a lightweight, modular, and scalable deep learning framework. Building on the original [Caffe](http://caffe.berkeleyvision.org/), Caffe2 is designed with expression, speed, and modularity in mind.

Caffe2.ai mention that "We’d love to start by saying that we really appreciate your interest in Caffe2, and hope this will be a high-performance framework for your machine learning product uses. Caffe2 is intended to be modular and facilitate fast prototyping of ideas and experiments in deep learning. Given this modularity, note that once you have a model defined, and you are interested in gaining additional performance and scalability, you are able to use pure C++ to deploy such models without having to use Python in your final product. Also, as the community develops enhanced and high-performance modules you are able to easily swap these modules into your Caffe2 project."


Required
------------------------------
```
1->CUDA version 10.2 
2->CUDNN version > 8.x 
3->OpenCV version = 4.1 
```
CMake Command
------------------------------
```
   mkdir caffe2_build 
   cd caffe2_build
   cmake -DBUILD_SHARED_LIBS:BOOL=ON -DCMAKE_BUILD_TYPE:STRING=Release -DPYTHON_EXECUTABLE:PATH=`which python3` -DCMAKE_INSTALL_PREFIX:PATH=../caffe_install ../caffe2
   cmake --build . --target install
```

# Different Cuda and OpenCV version, make change in below file

To change OpenCV version, you need to make changes to the following file
```
   caffe2/image/image_input_op.h
```
To change CUDNN version, you need to make changes to the following file. 
```
   caffe2/operators/conv_op_cudnn.cc
   caffe2/operators/recurrent_op_cudnn.cc
   caffe2/operators/conv_transpose_op_cudnn.cc
```

#
This library extract from [PyTorch](https://github.com/pytorch/pytorch) Library which was developed by Facebook AI Research (FAIR) <br />
Get some help from [caffe2 old release](https://github.com/facebookarchive/caffe2)
Caffe2 library tested in Nvidia GeForce RTX 2060 and Jetson Boards such as AGX Xavier, Nx and Tx2 <br />

NOTE: Getting any error, send me email and I can help you
