# Caffe2

Caffe2 is a lightweight, modular, and scalable deep learning framework. Building on the original [Caffe](http://caffe.berkeleyvision.org/), Caffe2 is designed with expression, speed, and modularity in mind.

Caffe2.ai mention that "We’d love to start by saying that we really appreciate your interest in Caffe2, and hope this will be a high-performance framework for your machine learning product uses. Caffe2 is intended to be modular and facilitate fast prototyping of ideas and experiments in deep learning. Given this modularity, note that once you have a model defined, and you are interested in gaining additional performance and scalability, you are able to use pure C++ to deploy such models without having to use Python in your final product. Also, as the community develops enhanced and high-performance modules you are able to easily swap these modules into your Caffe2 project."


# Required Environment
1->CUDA version 10.2  <br />
2->CUDNN version > 8.x  <br />
3->OpenCV version = 4.5.5  <br />

# CMake Command
mkdir caffe2_build  <br />
cd caffe2_build  <br />
cmake -DBUILD_SHARED_LIBS:BOOL=ON -DCMAKE_BUILD_TYPE:STRING=Release -DPYTHON_EXECUTABLE:PATH=`which python3` -DCMAKE_INSTALL_PREFIX:PATH=../caffe_install ../caffe2  <br />
cmake --build . --target install  <br />

This library extract from PyTorch Library which was developed by Facebook AI Research (FAIR) <br />
Caffe2 library tested in Nvidia AGX Xavier environment <br />

NOTE: When you use different environment and getting any error, send me email and I can help you