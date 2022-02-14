# Caffe2

Caffe2 is a lightweight, modular, and scalable deep learning framework. Building on the original [Caffe](http://caffe.berkeleyvision.org/), Caffe2 is designed with expression, speed, and modularity in mind.

Caffe2.ai mention that "We’d love to start by saying that we really appreciate your interest in Caffe2, and hope this will be a high-performance framework for your machine learning product uses. Caffe2 is intended to be modular and facilitate fast prototyping of ideas and experiments in deep learning. Given this modularity, note that once you have a model defined, and you are interested in gaining additional performance and scalability, you are able to use pure C++ to deploy such models without having to use Python in your final product. Also, as the community develops enhanced and high-performance modules you are able to easily swap these modules into your Caffe2 project."


# Required
1->CUDA version 10.2  <br />
2->CUDNN version > 8.x  <br />
3->OpenCV version = 4.5.5  <br />

# CMake Command
-mkdir caffe2_build  <br />
-cd caffe2_build <br />
-cmake -DBUILD_SHARED_LIBS:BOOL=ON -DCMAKE_BUILD_TYPE:STRING=Release -DPYTHON_EXECUTABLE:PATH=`which python3` -DCMAKE_INSTALL_PREFIX:PATH=../caffe_install ../caffe2 <br />
-cmake --build . --target install  <br />

# Different Cuda and OpenCV version, follow below Changes
I have made code changes in fo OpenCV

`caffe2/image/image_input_op.h`  <br />

I have made code changes in fo cudnn8

`caffe2/operators/conv_op_cudnn` <br />
`caffe2/operators/recurrent_op_cudnn.cc` <br />
`caffe2/operators/conv_transpose_op_cudnn.cc` <br />

#
This library extract from [PyTorch](https://github.com/pytorch/pytorch) Library which was developed by Facebook AI Research (FAIR) <br />
Get some help from [caffe2 old release](https://github.com/facebookarchive/caffe2)
Caffe2 library tested in Nvidia AGX Xavier <br />

NOTE: Getting any error, send me email and I can help you
