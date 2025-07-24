# IDS---Insect-Defense-System
A low cost, laser-based defense system against small insects.
Built for Raspberry Pi.

This Raspberry Pi-based defense system is used to shoot down small flying insects (e.g. mosquitoes) using a laser.
The system utilizes real-time scheduling to ensure that the system targets the insects in a timely manner and image recognition to detect insects and their positions.
Since the system relies on camera technology, the system does not work in dark environments.
For future updates, the system will be equiped with LiDAR and microphones to better detect and determine their positions.

## Setup
It's important to use the correct hardware and software.
Otherwise, the system is not guaranteed to work.
However, there are plenty of alternatives that work sufficiently.

### Hardware
It is especially important to use the same hardware, as the system implements a real-time scheduler to ensure certain deadlines are met.
Without these deadlines, we cannot guarantee that we can compute certain things and make physical actions in time.
The hardware, such as the camera and Raspberry Pi, must make their respective computations within these deadlines, and therefore, these components cannot be easily replaced.

- Raspberry Pi 3 Model B+

### Software
- Ubuntu 22.04 (_this was the development platform, but IDS works on other Ubuntu versions or Linux distributions too_)
- CMake 3.22 (`apt install cmake`)
- OpenCV (`apt install libopencv-dev`)
- C++ 20

### Building Project
From the project root, run the following commands.

```bash
mkdir build/
cmake -B build/
cmake --build build/ -j --target ids
```

You can now find the IDS executable in `build/ids`, which you can transfer to your Raspberry Pi (e.g. via SSH) and execute it.