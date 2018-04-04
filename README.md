# boost_arm-linux-gnueabihf

Cross compile C++ Library __BOOST__

## Download File
```bash
wget https://dl.bintray.com/boostorg/release/1.66.0/source/boost_1_66_0.tar.gz
tar xvf boost_1_66_0.tar.gz
cd boost_1_66_0
```

## Compile
```bash
./bootstrap  #generate project-config.jam
vi project-config.jam
```
> :12 
```
if ! gcc in [ feature.values <toolset> ]
{
using gcc : arm : arm-linux-gnueabihf-g++ ;
}
```
> :wq
```bash
sudo ./bjam install toolset=gcc-arm --prefix=/usr/local/boost-arm
```
