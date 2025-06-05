``` bash
source /opt/ros/jazzy/setup.bash
export RMW_IMPLEMENTATION=rmw_cyclonedds_cpp

ros2 launch scout_navigation nav2_scout_mini.launch.py
```

``` bash
source /opt/ros/jazzy/setup.bash

cd ~/scout_val_ws/src/scout-gz/scout_navigation/scripts$
python3 gt.py 
```

``` bash
zenohd
```

``` bash
source /opt/ros/jazzy/setup.bash
export RMW_IMPLEMENTATION=rmw_cyclonedds_cpp

cd PATH_TO_EXTRACTED_ZENOH_BRIDGE
./zenoh-bridge-ros2dds -c ~/ff_ws/src/free_fleet/free_fleet_examples/config/zenoh/nav2_scout_zenoh_bridge_ros2dds_client_config.json5
```

``` bash
source ~/ff_ws/install/setup.bash

ros2 run free_fleet_examples nav2_get_tf.py --namespace scout
```

``` bash
source ~/ff_ws/install/setup.bash
export ROS_DOMAIN_ID=55

ros2 launch free_fleet_examples scout_mini_rmf_common.launch.xml
```

``` bash
source ~/ff_ws/install/setup.bash
export ROS_DOMAIN_ID=55

ros2 launch free_fleet_examples nav2_scout_simulation_fleet_adapter.launch.xml 
```


``` bash
source ~/ff_ws/install/setup.bash
export ROS_DOMAIN_ID=55

ros2 run rmf_demos_tasks dispatch_patrol \
  -p north_west north_east south_east south_west \
  -n 2 \
  -st 0
```