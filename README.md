# Modified Patchwork ++
This repo contain personal modification of patchwork++ created by Lee et al (2022). Check the original paper at [arXiv](https://arxiv.org/abs/2207.11919) and [IEEE Xplore](https://ieeexplore.ieee.org/document/9981561). The modification only change the input data from *.bin file into *.pcd also add function to export ground after segmentation. For complete use and explanation, please check the [original repo](https://github.com/url-kaist/patchwork-plusplus)

## Tested Environment
- Ubuntu 22.04.2
- CMake 3.22.1
- Open3D 0.17.0
- Eigen 3.4.0

## Requirement
```
# To install Eigen and numpy
$ sudo apt-get install libeigen3-dev
$ pip install numpy

# To install Open3D Python packages
$ pip install open3d

# To install Open3D C++ packages
$ git clone https://github.com/isl-org/Open3D
$ cd Open3D
$ util/install_deps_ubuntu.sh # Only needed for Ubuntu
$ mkdir build && cd build
$ cmake ..
$ make # If it fails, try several times or try 'sudo make'
$ sudo make install
```
Or
```
# Install prerequisite packages including Open3D
$ git clone https://github.com/url-kaist/patchwork-plusplus
$ cd patchwork-plusplus
$ bash scripts/install_open3d.bash
```

## Build
```
# in patchwork-plusplus directory
$ mkdir build && cd build
$ cmake ..
$ make
```

## How to Run
```
# Run patchwork++ with your point cloud file, example here
$ ./build/examples/cpp/demo_visualize ./data/000000.pcd # specify file path
```

# Citation
Please cite the original paper of Patchwork++:

Patchwork++ ([arXiv](https://arxiv.org/abs/2207.11919), [IEEE Xplore](https://ieeexplore.ieee.org/document/9981561))

```
@inproceedings{lee2022patchworkpp,
    title={{Patchwork++: Fast and robust ground segmentation solving partial under-segmentation using 3D point cloud}},
    author={Lee, Seungjae and Lim, Hyungtae and Myung, Hyun},
    booktitle={Proc. IEEE/RSJ Int. Conf. Intell. Robots Syst.},
    year={2022},
    pages={13276-13283}
}
```

Patchwork [arXiv](https://arxiv.org/abs/2108.05560), [IEEE Xplore](https://ieeexplore.ieee.org/document/9466396)

```
@article{lim2021patchwork,
    title={Patchwork: Concentric Zone-based Region-wise Ground Segmentation with Ground Likelihood Estimation Using a 3D LiDAR Sensor},
    author={Lim, Hyungtae and Minho, Oh and Myung, Hyun},
    journal={IEEE Robotics and Automation Letters},
    year={2021}
}
```
