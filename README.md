### This is the current configuration for my Mx Master 3s Mouse, this configure all buttons and adds extra functionality like gesture, using the thumbwheel as volume controller

# mx-master-3s-config - You need to clone the repo
[logiops-githublink](https://github.com/PixlOne/logiops)

## Dependencies Needed: 

```bash
sudo dnf install cmake libevdev-devel systemd-devel libconfig-devel gcc-c++ glib2-devel
```
## Build the project:

```bash
mkdir build
cd build
cmake -DCMAKE_BUILD_TYPE=Release ..
make
```

## Build the package and enable the service for startup and reboot:

To install, run sudo make install after building. You can set the daemon to start at boot by running `sudo systemctl enable logid` or `sudo systemctl enable --now logid` if you want to enable and start the daemon.

## Finally add the the code in logid.cfg 

```bash
touch /ect/logid.cfg &&
sudo nano /etc/logid.cfg
```
