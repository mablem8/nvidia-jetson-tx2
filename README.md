In order to use the NVIDIA Jetson TX2 Tegra X2 Pascal GPU, you must install
software using an auxiliary Ubuntu 16.04 x86_64 computer.

An overview of the Getting Started process is available at the following URL:
https://developer.nvidia.com/embedded/learn/getting-started-jetson

Further details may be found at the following URL:
https://github.com/dusty-nv/jetson-inference#system-setup

A full JetPack install guide is available at the following URL:
https://docs.nvidia.com/jetpack-l4t/index.html#developertools/mobile/jetpack/l4t/3.0/jetpack_l4t_install.htm

The first step in getting started is to download the latest JetPack software to
the auxiliary computer from the following URL:
https://developer.nvidia.com/embedded/jetpack

In order to download the JetPack software, you must be signed into you NVIDIA
developer account.

After downloading JetPack, execute the following commands:

```bash
$ cd <directory where you downloaded JetPack>
$ chmod +x JetPack-L4T-<version>-linux-x64.run 
$ ./JetPack-L4T-<version>-linux-x64.run 
```

Follow the step-by-step GUI install guide. It is recommended to use the default
installation options in order to ensure that all tools are properly installed on
the Jetson board.

Note that JetPack will be installed in a directory on the auxiliary computer.
Specify the directory. Many large files will be downloaded to the auxiliary
computer during installation preparation. Parts of the installation process take
place in an in-GUI terminal.

The Jetson board will need to be connected to the auxiliary computer directly
via Ethernet cable or indirectly through a switch. Indirectly through a switch
is easier.

After auxiliary computer installation completes, connect the Jetson board to the
auxiliary computer with a micro-USB cable. Put the Jetson board into recovery
mode by holding down the recovery button while pressing and releasing reset.
After the Jetson board enters recovery mode, `lsusb` should list an NVIDIA
device. The Post Installation terminal window will guide you through this
process.

A 30 GB volume may mount onto the auxiliary computer while the Jetson board is
being flashed. After flashing is complete and before determining the Jetson
board IP address, an L4T volume may mount onto the auxiliary computer. Note
that, if the Jetson board is connected to the university network, its MAC
address must be registered with the university before the IP address discovery
process can succeed.

Once installation of target components finishes, close the XTerm window to
continue.

Test the Jetson board by booting into the system and running some sample code.
Samples can be found in the following directory:

```
/home/ubuntu/NVIDIA_CUDA-<version>_Samples/bin/aarch64/linux/release/
```

Try running the `oceanFFT` sample.

Other things to setup the Jetson:
* Software updates and `autoremove`
* Set the time zone
* Consider turning off the CUPS service
