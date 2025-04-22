# Major tasks

-   Cloned turtlesim
-   need to add collision awareness between multiple turtles
-   Expand the window - right now shows only small window
-   Add obstacles
-   Add collision awareness for obstacles
-   implement path planning algorithms from https://github.com/sanjana-dev9/path_planning_algorithms

# Sub-tasks

-   Cloned turtlesim

    -   Cloned ros_tutorial but with turtlesim folder
        ```
        git clone -n --depth=1 --filter=tree:0 https://github.com/zhangrelay/ros2_tutorials
        cd ros2_tutorials
        git sparse-checkout set --no-cone /turtlesim
        git checkout
        ```
    -   Build the package
    -   Basic commands

        ```
        ros2 run turtlesim turtlesim_node //Run turtelsim
        ros2 service call /spawn turtlesim/srv/Spawn '{x: 1.0, y: 1.0, theta: 0.0, name: "turtle2"}' // Add turtles
        ros2 run turtlesim turtle_teleop_key --ros-args --remap turtle1/cmd_vel:=turtle2/cmd_vel // telop with remapping
        ros2 launch turtlesim/launch/multisim.launch.py // multiple turtle sim window
        ```

-   Add collision awareness between multiple turtles
