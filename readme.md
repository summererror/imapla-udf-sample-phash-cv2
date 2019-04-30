# Impala UDF for pHash (C++ Edition)


## License
- [x] ["Anti 996" License](https://github.com/996icu/996.ICU/blob/master/LICENSE)
- [ ] ["Anti 995" License]
- [ ] ["Follow 955" License]
- [ ] ["World Peace" License] Sri Lanka Bombing


- So, I'm waiting for the three licenses above to republic.


## Background

Use [impala-udf-sample](https://github.com/cloudera/impala-udf-samples) to Create an Impala UDF function for image's phash compute based on cv::img_hash::pHash.
provided by  [opencv-> pHash](https://docs.opencv.org/4.1.0/df/d4e/classcv_1_1img__hash_1_1PHash.html) .






## Speed

0.5s/image, so, it's UNusable in produtive envirment abviously.
Luck!


## Install

### 1. Opencv

Refer to [Installation in Linux](https://docs.opencv.org/4.1.0/d7/d9f/tutorial_linux_install.html) .

#### 1.1 ffmpge
```shell
# Maybe you need configure the "mirror" for yum install.
sudo yum -y install ffmpeg ffmpeg-devel
```

#### 1.2 cmake (>3.x)
```shell
cd /tmp
wget https://github.com/Kitware/CMake/releases/download/v3.14.3/cmake-3.14.3-Linux-x86_64.tar.gz
tar xzf cmake-3.14.3-Linux-x86_64.tar.gz
```

#### 1.3 opencv(BASE) opencv_contrib(EXTRA)
```shell
cd /tmp
# opencv 4.1.0 download
wget https://github.com/opencv/opencv/archive/4.1.0.zip
unzip 4.1.0.zip
# opencv_contrib download from https://github.com/opencv/opencv_contrib
git clone https://github.com/opencv/opencv_contrib.git
cd opencv-4.1.0
mkdir build; cd build
# cmake
../../cmake-3.*/bin/cmake  -DCMAKE_BUILD_TYPE=Release -DCMAKE_INSTALL_PREFIX=/usr/local -DOPENCV_EXTRA_MODULES_PATH=../../opencv_contrib/modules/ ..
# make
make -j8
# install
make install
```

#### 1.4 cloudera 



