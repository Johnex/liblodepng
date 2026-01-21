# liblodepng
Extend LodePNG with CMake letting you build shared/static libraries

## Compiling
```bash
sudo apt install cmake g++ ninja-build -y
git clone --recursive https://github.com/Johnex/liblodepng.git
mkdir liblodepng/build
pushd liblodepng/build > /dev/null
cmake -G"Ninja" ..
ninja
sudo ninja install
popd > /dev/null
```

## Install Paths
```bash
johnex@JohnexCluster1~/liblodepng/build$ sudo ninja install
[sudo] password for johnex: *****************
[0/1] Install the project...
-- Install configuration: ""
-- Installing: /usr/local/include/lodepng.h
-- Installing: /usr/local/lib/liblodepng.so
-- Installing: /usr/local/lib/liblodepng-static.a
```
