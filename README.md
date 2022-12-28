# HumanBehaviorDetection_Paddle

## Usage

+ to modify model used in this project, you can open file: cmake/settings_options.cmake and modify its ${THIS_PROJECT_WINDOW_TITLE} for 4 algorithms embedded or you can specify model name in file: cmake/setting_process.cmake, with 'INFER_MODEL_DIR' string.

+ you should download inference libs after reading file paddle-inference/cpu-*/README.txt and place unzipped file to  paddle-inference folder, and modify 'PADDLE_DIR' string in cmake/settings_options.cmake

+ you can use this deploy example with CPU/GPU support, naively it will use CPU, if you intend to use GPU, remeber to modify 'WITH_GPU' to ON and 'CUDA_LIB'/'CUDNN_LIB' to folders that contains libcudart.so*/libcudnn.so*

+ if you use AMD CPU, then the performance of CPU computation may degenerate, in such case you should use BLAS-version inference lib and turn 'WITH_MKL' to OFF (default is ON).

+ if you would like to use this in windows platform, you must compile opencv using MSVC, and specify its build dir to 'OPENCV_DIR' in cmake/settings_options.cmake

+ windows platform building is not officially tested, but the author believe it will compile success without too much dirty work.

+ this project uses qt5, so you must install qt if you want to use this, on ubuntu-like os, you can simply install dependencies using scripts in script folder.


## Contributors

+ Guangfu Wang: thuwgf@gmail.com

+ Pengpeng Yan: yanpp20170507@163.com


## License

MIT LICENSE  for Research purpose.

for Commercial usage please  contact: thuwgf@gmail.com


