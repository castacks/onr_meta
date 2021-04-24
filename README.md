# ONR Metarepo

## Setting up the workspace

First install vstool 

```
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
sudo apt-key adv --keyserver hkp://pool.sks-keyservers.net --recv-key 0xAB17C654
sudo apt-get update
sudo apt-get install python3-vcstool
```

Then we can setup the workspace with
```
mkdir -p ~/onr_ws/src
cd ~/onr_ws/src
git clone git@bitbucket.org:castacks/onr_meta.git
vcs import < onr_meta/onr_ws.repo
```

Vcs has many tools for working with multiple repos. For example, you can run commands such as ```vcs status``` which runs `git status` in all repos. 

You can add additional repos to the onr_meta.repo file as you add them to your workspace.