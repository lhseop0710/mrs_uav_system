# Multi-robot Systems Group UAV system
![thumbnail](.fig/drone_collage.jpg)

The [Multi-robot Systems Group](http://mrs.felk.cvut.cz) is a robotics lab at the [Czech Technical University in Prague](https://www.cvut.cz/).
We mostly work with multi-rotor helicopters, and for them specifically, we develop this control, estimation, and simulation platform.
We think that real-world and replicable experiments should support excellent research and science in robotics.
Thus our platform is built to allow safe verification of approaches in planning, control, estimation, computer vision, tracking, and more.

## Meta-repositories

These meta-repositories aggregate related packages.

| Component                                                                       | 20.04                                                                                                                                                          | Description                                                                                                        |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [mrs_uav_system](https://github.com/ctu-mrs/mrs_uav_system)                     | [![Build Status](https://github.com/ctu-mrs/mrs_uav_system/workflows/Noetic/badge.svg)](https://github.com/ctu-mrs/mrs_uav_system/actions)                     | Integrates [uav_core](https://github.com/ctu-mrs/uav_core) and [simulation](https://github.com/ctu-mrs/simulation) |
| [uav_core](https://github.com/ctu-mrs/uav_core)                                 | [![Build Status](https://github.com/ctu-mrs/uav_core/workflows/Noetic/badge.svg)](https://github.com/ctu-mrs/uav_core/actions)                                 | The minimum needed to fly a drone                                                                                  |
| [simulation](https://github.com/ctu-mrs/simulation)                             | [![Build Status](https://github.com/ctu-mrs/simulation/workflows/Noetic/badge.svg)](https://github.com/ctu-mrs/simulation/actions)                             | Simulation resources                                                                                               |
| [uav_modules](https://github.com/ctu-mrs/uav_modules)                           | [![Build Status](https://github.com/ctu-mrs/uav_modules/workflows/Noetic/badge.svg)](https://github.com/ctu-mrs/uav_modules/actions)                           | Optional UAV modules, drivers and utils                                                                            |
| [octomap_mapping_planning](https://github.com/ctu-mrs/octomap_mapping_planning) | [![Build Status](https://github.com/ctu-mrs/octomap_mapping_planning/workflows/Noetic/badge.svg)](https://github.com/ctu-mrs/octomap_mapping_planning/actions) | Octomap Mapping & Planning for UAVs                                                                                |
| [linux-setup](https://github.com/klaxalk/linux-setup)                           | [![Build Status](https://github.com/klaxalk/linux-setup/workflows/Focal/badge.svg)](https://github.com/klaxalk/linux-setup/actions)                            | Tomas's Linux configuration                                                                                        |

## System properties

The platform is

* built using [Robot Operating System](https://www.ros.org/) Noetic,
* meant to be executed entirely onboard,
* can be deployed on any multi-rotor vehicle, given it is equipped with a [PX4](https://github.com/ctu-mrs/px4_firmware)-compatible [flight controller](https://pixhawk.org/),
* for both indoor and outdoor,
* supports multi-robot experiments using [Nimbro network](https://github.com/ctu-mrs/nimbro_network) communication.
* provides both: agile flying and robust control.

![](https://github.com/ctu-mrs/mrs_uav_system/raw/gifs/gazebo_circle.gif)

## [Documentation](https://ctu-mrs.github.io/)

The primary source of documentation is here: [https://ctu-mrs.github.io/](https://ctu-mrs.github.io/).
However, the website only scratches a surface of what it should contain (and we know it).
Our system is a research-oriented platform, and it evolves rapidly.
Most of our users are either researchers (who already know the platform) or freshmen students (who might not know ROS at all).
Maintaining up-to-date documentation for such an audience is hard work, since we mostly spend our time developing the system while using it for our research.
So instead, we aim at educating our students to look around the packages (each contains its own README), explore the launch files and be able to read the code, which we strive to keep readable.

[![](https://github.com/ctu-mrs/mrs_uav_system/raw/diagram/mrs_uav_system_diagram.jpg)](https://github.com/ctu-mrs/mrs_uav_system/raw/diagram/mrs_uav_system_diagram.pdf)

The system follows a description presented in the article [doi.org/10.1007/s10846-021-01383-5](https://doi.org/10.1007/s10846-021-01383-5), [pdf](https://link.springer.com/content/pdf/10.1007/s10846-021-01383-5.pdf):
```
Baca, T., Petrlik, M., Vrba, M., Spurny, V., Penicka, R., Hert, D., and Saska, M.,
"The MRS UAV System: Pushing the Frontiers of Reproducible Research, Real-world Deployment, and
Education with Autonomous Unmanned Aerial Vehicles", J Intell Robot Syst 102, 26 (2021).
```

## Unmanned Aerial Vehicles

The MRS UAV system is currently pre-configured for the following UAV platforms, operated by the MRS.
The platforms are order by the size / payload capacity.

| Model        | Simulation                    | Real UAV                      |
|--------------|-------------------------------|-------------------------------|
| DJI f330     | ![](.fig/f330_simulation.jpg) | ![](.fig/f330_real.jpg)       |
| DJI f450     | ![](.fig/f450_simulation.jpg) | ![](.fig/f450_real.jpg)       |
| Holybro x500 | ![](.fig/x500_simulation.jpg) | ![](.fig/x500_real.jpg)       |
| DJI f550     | ![](.fig/f550_simulation.jpg) | ![](.fig/f550_real.jpg)       |
| Tarot t650   | ![](.fig/t650_simulation.jpg) | ![](.fig/t650_real.jpg)       |
| NAKI II      | ![](.fig/naki_simulation.jpg) | ![](.fig/naki_real.jpg)       |

## Related packages

The following packages are not necessarily part of our automated installation.
Therefore, you might need to clone them by yorself and place in your ROS workspace.
Some of those are forks of third party repositories.

| Package                                                                              | Description                                                                                   | 20.04                                                                                                                                                                |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MRS Gazebo Extra Resources](https://github.com/ctu-mrs/mrs_gazebo_extras_resources) | *MRS System*-depended optional plugins and resources                                          | [![Build Status](https://github.com/ctu-mrs/mrs_gazebo_extras_resources/workflows/Noetic/badge.svg)](https://github.com/ctu-mrs/mrs_gazebo_extras_resources/actions) |
| [Example ROS packages](https://github.com/ctu-mrs/example_ros_packages)              | MRS ROS examples                                                                              | [![Build Status](https://github.com/ctu-mrs/example_ros_packages/workflows/Noetic/badge.svg)](https://github.com/ctu-mrs/example_ros_packages/actions)               |
| [Nimbro network](https://github.com/ctu-mrs/nimbro_network)                          | ROS communication layer for multiple independent machines                                     | [![Build Status](https://github.com/ctu-mrs/nimbro_network/workflows/Noetic/badge.svg)](https://github.com/ctu-mrs/nimbro_network/actions)                           |
| [MRS optic flow](https://github.com/ctu-mrs/mrs_optic_flow)                          | GPU-accelerated optic flow alorithm for UAV odometry                                          | [![Build Status](https://github.com/ctu-mrs/mrs_optic_flow/workflows/Noetic/badge.svg)](https://github.com/ctu-mrs/mrs_optic_flow/actions)                           |
| [Hector SLAM](https://github.com/tu-darmstadt-ros-pkg/hector_slam)                   | 2D Laser-based LIDAR SLAM, [how to](https://ctu-mrs.github.io/docs/software/hector_slam.html) |                                                                                                                                                                      |
| [Hector SLAM](https://github.com/ctu-mrs/hector_slam) - MRS fork                     | + Nodeleted, [how to](https://ctu-mrs.github.io/docs/software/hector_slam.html)               | [![Build Status](https://github.com/ctu-mrs/hector_slam/workflows/Noetic/badge.svg)](https://github.com/ctu-mrs/hector_slam/actions)                                 |
| [MRS Serial](https://github.com/ctu-mrs/mrs_serial)                                  | serial line interface to ROS, communicates using the BACA protocol                            | [![Build Status](https://github.com/ctu-mrs/mrs_serial/workflows/Noetic/badge.svg)](https://github.com/ctu-mrs/mrs_serial/actions)                                   |
| [UVDAR](https://github.com/ctu-mrs/uvdar)                                            | mutual localization of UAVs using Ultra-Violet LED blinkers                                   | [![Build Status](https://github.com/ctu-mrs/uvdar_core/workflows/Noetic/badge.svg)](https://github.com/ctu-mrs/uvdar_core/actions)                                   |
| [UVDAR gazebo plugin](https://github.com/ctu-mrs/uvdar_gazebo_plugin)                | Gazebo plugin for UVDAR                                                                       | [![Build Status](https://github.com/ctu-mrs/uvdar_gazebo_plugin/workflows/Noetic/badge.svg)](https://github.com/ctu-mrs/uvdar_gazebo_plugin/actions)                 |
| [trajectory loader](https://github.com/ctu-mrs/trajectory_loader)                    | Loading UAV trajectories from CSV files                                                       | [![Build Status](https://github.com/ctu-mrs/trajectory_loader/workflows/Noetic/badge.svg)](https://github.com/ctu-mrs/trajectory_loader/actions)                     |
| [Bluefox2](https://github.com/ctu-mrs/bluefox2)                                      | MV Bluefox2 driver, MRS fork                                                                  | [![Build Status](https://github.com/ctu-mrs/bluefox2/workflows/Noetic/badge.svg)](https://github.com/ctu-mrs/bluefox2/actions)                                       |
| [Object detection](https://github.com/ctu-mrs/object_detect)                         | Object detection by color segmentation                                                        | [![Build Status](https://github.com/ctu-mrs/object_detect/workflows/Noetic/badge.svg)](https://github.com/ctu-mrs/object_detect/actions)                             |
| [MRS utils](https://github.com/ctu-mrs/mrs_utils)                                    | Development utils                                                                             | [![Build Status](https://github.com/ctu-mrs/mrs_utils/workflows/Noetic/badge.svg)](https://github.com/ctu-mrs/mrs_utils/actions)                                     |
| [OctomapTools](https://github.com/ctu-mrs/octomap_tools)                             | Octomap visualization and manipulation                                                        |                                                                                                                                                                      |
| [MBZIRC 2020 - Wall Building](https://github.com/ctu-mrs/mbzirc_2020_wall_building)  | System for automatic wall-building for MBZIRC 2020                                            | [![Build Status](https://github.com/ctu-mrs/mbzirc_2020_wall_building/workflows/Noetic/badge.svg)](https://github.com/ctu-mrs/mbzirc_2020_wall_building/actions)     |
| [Summer School 2019](https://github.com/ctu-mrs/mtsp_planning_task)                  | Summer School 2019 task - MTSP planning                                                       | [![Build Status](https://github.com/ctu-mrs/mtsp_planning_task/workflows/Noetic/badge.svg)](https://github.com/ctu-mrs/mtsp_planning_task/actions)                   |
| [Summer School 2020](https://github.com/ctu-mrs/leader_follower_task)                | Summer School 2020 task - UVDAR leader-follower                                               | [![Build Status](https://github.com/ctu-mrs/leader_follower_task/workflows/Noetic/badge.svg)](https://github.com/ctu-mrs/leader_follower_task/actions)               |
| [Summer School 2022](https://github.com/ctu-mrs/summer-school-2022)                  | Summer School 2022 task - Multirobotic inspection and monitoring                              | [![Build Status](https://github.com/ctu-mrs/summer-school-2022/workflows/Focal/badge.svg)](https://github.com/ctu-mrs/leader_follower_task/actions)                  |

## Backwards compatibility and updates

We do not guarantee backwards compatibility at any time.
The platform is evolving according to the needs of the MRS group.
Updates can be made that are not going to be compatible with users local configs, simulation worlds, tmux sessions, etc.
However, when we change something which requires user action to maintain compatibility, we will create an issue in this repository labelled **users-read-me**.
Subscribe to this repository updates and issues by clicking the **Watch** button in the top-right corner of this page.
Recent changes requiring user action:

* January 17, 2023: [Updates for px4 firmware v1.13.2](https://github.com/ctu-mrs/mrs_uav_system/issues/150)
* March 8, 2022: [mrs_lib::Transformer interface updated](https://github.com/ctu-mrs/mrs_uav_system/issues/136)
* December 09, 2021: [not building with --march=native anymore](https://github.com/ctu-mrs/mrs_uav_system/issues/126)
* December 25, 2020: [Updated controller interface, updated thrust curve parametrization](https://github.com/ctu-mrs/mrs_uav_system/issues/33)
* December 15, 2020: [Rework of simulation UAV spawning mechanism, Noetic update](https://github.com/ctu-mrs/mrs_uav_system/issues/32)
* November 12, 2020: [GPS coordinates within Gazebo world need changing](https://github.com/ctu-mrs/mrs_uav_system/issues/22)
* November 12, 2020: [Rangefinder fusion needs enabling in simulation sessions](https://github.com/ctu-mrs/mrs_uav_system/issues/21)

## Installation

### Singularity and Docker

Singularity images with our system are the preferred way how a _normal_ user should interract with our sustem.
Pleaase, follow this link to learn how to run our system using Singularity.

* [MRS Singularity](https://github.com/ctu-mrs/mrs_singularity/)

Our Singularity images are built almost completely from Docker images.
The following link points to our Docker HUB organization.

* [Docker Images](https://hub.docker.com/u/ctumrs)

### Native installation (not recommended)

Native installation is supported via a set of automated install scripts.
**Beware** the installation will take a **lot of disk space**, is **difficult to remove** from the computer, and is often **difficult to upgrade**.
The native installation is intended mostly for real drones.
Most people should use [MRS Singularity](https://github.com/ctu-mrs/mrs_singularity) for working with the MRS system!

In the you want a native installation case we provide installation scripts that set everything up for you.
Our automated install script will:
* install Robot Operating System (ROS),
* install other dependencies such *git*, *gitman*,
* clone [uav_core](https://github.com/ctu-mrs/uav_core), [simulation](https://github.com/ctu-mrs/simulation), [example_ros_packages](https://github.com/ctu-mrs/example_ros_packages) into *~/git*,
* install more dependencies such as *tmux* and *tmuxinator*
* create our ros workspace ([guide](https://ctu-mrs.github.io/docs/software/catkin/managing_workspaces/managing_workspaces.html)) in ```~/mrs_workspace``` for the *uav_core* and *simulation*,
* create a ros workspace in ```~/workspace``` for *examples* ([guide](https://ctu-mrs.github.io/docs/software/catkin/managing_workspaces/managing_workspaces.html)),
* link our packages to the workspaces ([guide](https://ctu-mrs.github.io/docs/software/catkin/managing_workspaces/managing_workspaces.html)),
* compile the workspaces,
* add configuration lines into your *~/.bashrc*.

To start the automatic installation, please paste the following code into your terminal and press **enter**.
You might be prompted a few times to confirm something by pressing enter:
```bash
cd /tmp
echo '
GIT_PATH=~/git
mkdir -p $GIT_PATH
cd $GIT_PATH
sudo apt-get -y install git
git clone https://github.com/ctu-mrs/mrs_uav_system
cd mrs_uav_system
git checkout master
git pull
./install.sh -g $GIT_PATH
source ~/.bashrc' > clone.sh && source clone.sh
```

#### "I already have ROS and just want to peek in"

If you already have ROS installed and if you are fluent with *workspaces*, *.bashrc*, *catkin tools*, etc., feel free to clone our repositories individually.
The [uav_core](https://github.com/ctu-mrs/uav_core) repository integrates our UAV control system.
Please follow its README for further instructions on how to install its particular dependencies.

The [simulation](https://github.com/ctu-mrs/simulation) repository provides resources for *Gazebo/ROS* simulation, including px4 Simulation-in-the-Loop (SITL), UAV models and useful sensor plugins.
Please follow its README for further instructions on how to install prerequisities.

#### "I want the Linux environment people from MRS works with"

Great! In that case you want to install Tomas's Linux-setup.
**Beware!** This might alter your existing configuration of some Linux tools (Vim, Tmux, i3wm, ranger, ...).
Refer to its [README](https://github.com/klaxalk/linux-setup), for more information.
Installation is *not* obligatory and the MRS UAV system will work without it.

Paste following code into your terminal and press **enter**
```bash
cd /tmp
echo "mkdir -p ~/git
cd ~/git
sudo apt-get -y install git
git clone https://github.com/klaxalk/linux-setup
cd linux-setup
./install.sh" > run.sh && source run.sh
```

For help with using the system, you can also refer to the [MRS Cheatsheet](https://ctu-mrs.github.io/docs/introduction/cheatsheet.html).

## Running the simulation

If you have successfully installed the system, you can continue with [starting the simulation](https://ctu-mrs.github.io/docs/simulation/howto.html).
