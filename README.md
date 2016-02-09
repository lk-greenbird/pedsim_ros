# `pedsim_ros`

![Crowd](/pedsim_simulator/images/crowd1.png?raw=true "Pedsim Crowd") ![Costmap](/pedsim_simulator/images/costmap.png?raw=true "Pedsim Costmap")


ROS meta package for PedSim (Pedestrian Simulator) based on social force
model of [Helbing et. al](http://arxiv.org/pdf/cond-mat/9805244.pdf). The implementation is based on a modified version of Christian Gloor's [libpedsim](http://pedsim.silmaril.org/) library which has been extended to include additional behaviors and activities. All visualization is done via [Rviz](http://wiki.ros.org/rviz).


### Requirements
- ROS (currently tested on `hydro`, `indigo` )
- C++11 compiler
- Qt4
- Eigen3

### Dependencies
* Pedsim library, available from [https://github.com/srl-freiburg/pedsim.git](https://github.com/srl-freiburg/pedsim.git)
* Animated markers available from [https://github.com/srl-freiburg/animated_markers](https://github.com/srl-freiburg/animated_markers)
* (**Optional**) Rviz additional costmap visualization colors (jet, hot, etc). Installable via our `rviz` fork from [https://github.com/srl-freiburg/rviz](https://github.com/srl-freiburg/rviz).
* (**Optional**) Rviz plugins for visualizing tracked people, groups, social relations, etc. See [plugin page for more details](https://github.com/spencer-project/spencer_people_tracking/tree/master/visualization/spencer_tracking_rviz_plugin)


### Installation
Clone into you catkin workspace, then catkin magic;

```
cd [workspace]/src
git clone https://github.com/srl-freiburg/pedsim.git
git clone https://github.com/srl-freiburg/pedsim_ros.git
# remaining clones are optional
git clone https://github.com/srl-freiburg/rviz.git
git clone https://github.com/srl-freiburg/animated_markers.git
git clone https://github.com/spencer-project/spencer_people_tracking.git
cd ..
catkin build -c
```

### Sample usage
```
roslaunch pedsim_simulator simple_pedestrians.launch
```

#### TODO
- [ ] Add additional crowd behaviours
- [ ] Scenario build tool (GUI)


### Developers
* Billy Okal
* Omar Islas
* Timm Linder


### Contributors
* Dizan Vasquez
* Sven Wehner

The package is a **work in progress** used in research prototyping. Pull requests and/or issues are highly encouraged.


