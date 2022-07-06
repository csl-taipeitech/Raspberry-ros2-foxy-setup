# EVpi-embedded

## Common used commands
1. Bringup can_manager
    ```bash
    ros2 launch evpi_bringup can_bringup.launch
    ```

## Prerequirements
1. Install ROS2 foxy

```bash
locale  # check for UTF-8
sudo apt update && sudo apt install locales
```

```bash
sudo locale-gen en_US en_US.UTF-8
sudo update-locale LC_ALL=en_US.UTF-8 LANG=en_US.UTF-8
export LANG=en_US.UTF-8
locale  # verify settings
apt-cache policy | grep universe
sudo apt install software-properties-common
sudo add-apt-repository universe
sudo apt update && sudo apt install curl gnupg2 lsb-release
```

```bash
sudo curl -sSL https://raw.githubusercontent.com/ros/rosdistro/master/ros.key  -o /usr/share/keyrings/ros-archive-keyring.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/ros-archive-keyring.gpg] http://packages.ros.org/ros2/ubuntu $(source /etc/os-release && echo $UBUNTU_CODENAME) main" | sudo tee /etc/apt/sources.list.d/ros2.list > /dev/null
sudo apt update
sudo apt upgrade
```

```bash
sudo apt install ros-foxy-ros-base
```

```bash
source /opt/ros/foxy/setup.bash
echo "source /opt/ros/foxy/setup.bash" >> .bashrc
```

2. Install can-util                                      
```bash
sudo apt-get install can-utils
```

3. Install other packages (optional) 
```bash
sudo apt install network-manager
sudo apt install net-tools
```
