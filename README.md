# slam_docker_collection

This is my personal attempt to create reusable and portable environments for 3D SLAM with docker.

## Basic Usage

Update submodule:
```bash
cd slam_docker_collection
git submodule init
git submodule update hdl_graph_slam
```

Build docker image:
```bash
cd slam_docker_collection/hdl_graph_slam/docker
./build.sh
```

Run docker image:
```bash
cd slam_docker_collection/hdl_graph_slam/docker
./run.sh -v ~/datasets:/datasets  # you can put more docker run arguments here

# in docker
roslaunch hdl_graph_slam hdl_graph_slam_400.launch
```

## Dockernized packages
| Build status | Package | Short Usage |
| ------------ | ------- | ----------- |
| [![Build Status](https://travis-ci.org/koide3/ethzasl_icp_mapping.svg?branch=reintegrate%2Fmaster_into_indigo_devel)](https://travis-ci.org/koide3/ethzasl_icp_mapping) | [ethzasl_icp_mapping](https://github.com/ethz-asl/ethzasl_icp_mapping) | [[usage]](https://github.com/koide3/ethzasl_icp_mapping/blob/reintegrate/master_into_indigo_devel/docker/howtouse.md) | ![ethzasl_icp](https://user-images.githubusercontent.com/31344317/98346757-c4bf9480-2059-11eb-93b0-d97dc637fe16.gif) |
| [![Build Status](https://travis-ci.org/koide3/hdl_graph_slam.svg?branch=master)](https://travis-ci.org/koide3/hdl_graph_slam) | [hdl_graph_slam](https://github.com/koide3/hdl_graph_slam) | [[usage]](https://github.com/koide3/hdl_graph_slam/blob/master/docker/howtouse.md) |
| [![Build Status](https://travis-ci.org/koide3/loam_velodyne.svg?branch=master)](https://travis-ci.org/koide3/loam_velodyne) | [LOAM](https://github.com/laboshinl/loam_velodyne) | [[usage]](https://github.com/koide3/loam_velodyne/blob/master/docker/howtouse.md) |
| [![Build Status](https://travis-ci.org/koide3/LeGO-LOAM-BOR.svg?branch=master)](https://travis-ci.org/koide3/LeGO-LOAM-BOR) | [LeGO-LOAM](https://github.com/RobustFieldAutonomyLab/LeGO-LOAM) | [[usage]](https://github.com/koide3/LeGO-LOAM-BOR/blob/master/docker/howtouse.md) |
| [![Build Status](https://travis-ci.org/koide3/SuMa.svg?branch=master)](https://travis-ci.org/koide3/SuMa) | [SuMa](https://github.com/jbehley/SuMa) | [[usage]](https://github.com/koide3/SuMa/blob/master/docker/howtouse.md) |
| [![Build Status](https://travis-ci.org/koide3/LINS---LiDAR-inertial-SLAM.svg?branch=master)](https://travis-ci.org/koide3/LINS---LiDAR-inertial-SLAM) | [LINS](https://github.com/ChaoqinRobotics/LINS---LiDAR-inertial-SLAM) | [[usage]](https://github.com/koide3/LINS---LiDAR-inertial-SLAM/blob/master/docker/howtouse.md) |
| [![Build Status](https://travis-ci.org/koide3/lio-mapping.svg?branch=master)](https://travis-ci.org/koide3/lio-mapping) | [LIO-mapping](https://github.com/hyye/lio-mapping) | [[usage]](https://github.com/koide3/lio-mapping/blob/master/docker/howtouse.md) |
| [![Build Status](https://travis-ci.org/koide3/LIO-SAM.svg?branch=master)](https://travis-ci.org/koide3/LIO-SAM) | [LIO-SAM](https://github.com/TixiaoShan/LIO-SAM) | [[usage]](https://github.com/koide3/LIO-SAM/blob/master/docker/howtouse.md) |
| [![Build Status](https://travis-ci.org/koide3/voxblox.svg?branch=master)](https://travis-ci.org/koide3/voxblox) | [Voxblox](https://github.com/ethz-asl/voxblox) | [[usage]](https://github.com/koide3/voxblox/blob/master/docker/howtouse.md) |
| [![Build Status](https://travis-ci.org/koide3/voxgraph.svg?branch=master)](https://travis-ci.org/koide3/voxgraph) | [Voxgraph](https://github.com/ethz-asl/voxgraph) | [[usage]](https://github.com/koide3/voxgraph/blob/master/docker/howtouse.md) |


| LOAM | hdl_graph_slam | SuMa |
| ---- | -------------- | ---- |
| <img style="max-height: 320pix; width: auto;" src="https://user-images.githubusercontent.com/31344317/98347880-5da2df80-205b-11eb-8aae-abfd8fc67f70.gif"/> | <img style="max-height: 320pix; width: auto;" src="https://user-images.githubusercontent.com/31344317/98347836-4fed5a00-205b-11eb-931c-158f6cd056bf.gif"/> | <img style="max-height: 320pix; width: auto;" src="https://user-images.githubusercontent.com/31344317/98347870-5bd91c00-205b-11eb-82f0-8dec94dc3aec.gif"/> |

| LINS | SuMa | voxgraph |
| ---- | ---- | -------- |
| <img style="max-height: 320pix; width: auto;" src="https://user-images.githubusercontent.com/31344317/98347847-54197780-205b-11eb-988b-ac497d3ec8f8.gif"/> | <img  style="max-height: 320pix; width: auto;" src="https://user-images.githubusercontent.com/31344317/98347890-60053980-205b-11eb-97fa-de73c2f9448f.gif"/> | <img style="max-height: 320pix; width: auto;" src="https://user-images.githubusercontent.com/31344317/98347899-64315700-205b-11eb-92d5-1f2df959af6f.gif"/> |
