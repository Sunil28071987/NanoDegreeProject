cmake_minimum_required(VERSION 3.7)
project(kf_p1)
set(CMAKE_CXX_STANDARD 11)
include_directories(/usr/local/Cellar/eigen/3.3.3/include/eigen3/)
include_directories(/usr/local/include)
   link_directories(/usr/local/lib)
include_directories(/usr/local/Cellar/openssl/1.0.2k/include)
   link_directories(/usr/local/Cellar/openssl/1.0.2k/lib)
include_directories(/usr/local/Cellar/libuv/1.11.0/include)
   link_directories(/usr/local/Cellar/libuv/1.11.0/lib)
include_directories(/usr/local/Cellar/zlib/1.2.11/include)
   link_directories(/usr/local/Cellar/zlib/1.2.11/lib)
add_executable(kf_p1 main.cpp kalman_filter.cpp FusionEKF.cpp tools.cpp)
target_link_libraries(kf_p1 z ssl uv uWS)