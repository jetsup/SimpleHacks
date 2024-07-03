# Alias

When working in with many environment on Linux, you have control of command should be active and how you want to reference them. For instance, I have multiple versions of ROS2, Humble and Iron, I find myself having to run the command:

```bash
source /opt/ros/humble/setup.zsh # for humble
# or
source /opt/ros/iron/setup.zsh # for iron
```

Apart from my terminal having history highlighting capability, I sometimes find it strenuous to run these, and I prefer short commands like `enable-ros-humble` or `enable-ros-iron`.

This is made possible by adding:

```bash
alias enable-ros-humble='. /opt/ros/humble/setup.zsh' # for humble
```

Also, with alias, you can execute multiple source commands with one alias, jus separate the two `source` with `&&`.

```bash
alias enable-ros-humble='. /opt/ros/humble/setup.zsh && . /usr/share/colcon_argcomplete/hook/colcon-argcomplete.zsh'
```

This is equivalent to running:

```bash
source /opt/ros/humble/setup.zsh
source /usr/share/colcon_argcomplete/hook/colcon-argcomplete.zsh
```
