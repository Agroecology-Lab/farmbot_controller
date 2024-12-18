
# FarmBot ROS Controller Documentation

The `farmbot_controller` is part of the FarmBot ROS ecosystem and is designed to interface with FarmBot hardware through the Robot Operating System 2 (ROS2). This package provides control over the FarmBot’s movement, sensors, and actions, enabling automated farming tasks in a ROS2 environment.

## Overview

The `farmbot_controller` package communicates with the FarmBot hardware and executes tasks based on ROS2 topics, services, and actions. It integrates with other ROS2 nodes and utilizes the capabilities of ROS2 for inter-process communication, scheduling, and lifecycle management.

## Repository Structure

- `config/`: Configuration files to customize the controller for your specific setup.
- `launch/`: ROS2 launch files to start the controller node and related components.
- `src/`: Source code for the controller implementation.
- `CMakeLists.txt`: CMake configuration for building the package.
- `package.xml`: Defines dependencies and metadata for the ROS2 package.

## Prerequisites

Before setting up the `farmbot_controller` package, ensure the following:

- **ROS2 Installation**: Install ROS2 on your system. Instructions can be found in the [ROS2 installation guide](https://docs.ros.org/en/foxy/Installation.html).
- **FarmBot Hardware**: A fully operational FarmBot setup is required.
- **Dependencies**: Ensure that all dependencies are met as defined in the `package.xml`.

## Installation

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/farmbot-ros/farmbot_controller.git
   ```

2. **Build the Package Using Colcon**:

   Navigate to your ROS2 workspace and build the package with `colcon`:

   ```bash
   cd ~/ros2_ws
   colcon build --packages-select farmbot_controller
   ```

3. **Source the Workspace**:

   After the build process completes, source the workspace to make the controller available:

   ```bash
   source ~/ros2_ws/install/setup.bash
   ```

## Configuration

Customize the `farmbot_controller` by editing configuration files located in the `config/` directory. Make sure to adjust parameters to match your specific FarmBot hardware and setup needs.

## Usage

### Launching the Controller

To launch the FarmBot controller, use the following ROS2 launch command:

```bash
ros2 launch farmbot_controller controller.launch.py
```

This command starts the controller node and establishes communication between ROS2 and the FarmBot hardware.

### Controlling the FarmBot

Once the controller is running, you can send commands and interact with the FarmBot through ROS2 topics, services, and actions.

## Contributing

We welcome contributions! To contribute to the `farmbot_controller`:

1. Fork the repository.
2. Create a new feature branch.
3. Implement your changes and submit a pull request.

Please ensure that your code adheres to the ROS2 coding standards and passes tests.

## Support

For questions or issues, please open an issue in the GitHub repository, and we'll do our best to help.

## License

The `farmbot_controller` package is open-source and released under the MIT License. See the `LICENSE` file for more details.

