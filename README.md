# SFUISE (Spline Fusion-Based Ultra-Wideband-Inertial State Estimation)
## -- Continuous-Time Ultra-Wideband-Inertial Fusion
This is the code repository of SFUISE, a continuous-time ultrawideband-inertial fusion system. 
![eval_util](https://github.com/kailaili/sfuiseRelease/blob/main/doc/util_sequences.gif)
## BibTex Citation
## Dependency
System dependencies (tested on Ubuntu 20.04)
* [Eigen](https://eigen.tuxfamily.org/index.php?title=Main_Page) (tested with Eigen 3.3.7)
* [SuiteSparse](https://people.engr.tamu.edu/davis/suitesparse.html)
## Compilation
Compile with [catkin_tools](https://catkin-tools.readthedocs.io/en/latest/index.html):
```
cd ~/catkin_ws/src
git clone https://github.com/KIT-ISAS/SFUISE
cd ..
catkin build sfuise
```
## Usage
Run following commands in terminal
* Example for running sfuise on [UTIL](https://utiasdsl.github.io/util-uwb-dataset/):
```
# Change anchor_path in config_test_util.yaml
roslaunch sfuise sfuise_test_util.launch
rosbag play const1-trial1-tdoa2.bag
```
* Example for running sfuise on [ISAS-Walk](https://github.com/kailaili/sfuiseRelease/tree/main/dataset):
```
roslaunch sfuise sfuise_test_isas-walk1.launch
rosbag play ISAS-Walk1.bag
```
## Contributors
Kailai Li (Email: kailai.li@liu.se)

Ziyu Cao (Email: ziyu.cao@kit.edu)
## Credits
We hereby recommend reading [lie-spline-experiments](https://gitlab.com/tum-vision/lie-spline-experiments) for reference. The IMU integration was derived from [VINS-Fusion](https://github.com/HKUST-Aerial-Robotics/VINS-Fusion).
## License
The source code is released under [GPLv3](https://www.gnu.org/licenses/) license.

We are constantly working on improving our code. For any technical issues, please contact 
Kailai Li (kailai.li@liu.se).