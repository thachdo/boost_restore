### Recover to boost 1.65 (ubunbu 18.04) after installing a newer boost version
Check the current boost version
```
cat /usr/include/boost/version.hpp | grep "BOOST_LIB_VERSION"
```

Backup the current boost version
```
mkdir usr_include_boost_bk && \
sudo cp -r /usr/include/boost/ ./usr_include_boost_bk && \
mkdir usr_lib_x86_64-linux-gnu_bk && \
sudo cp /usr/lib/x86_64-linux-gnu/libboost* ./usr_lib_x86_64-linux-gnu_bk && \
mkdir usr_local_include_boost_bk && \
cp -r /usr/local/include/boost ./usr_local_include_boost_bk && \
mkdir  ./usr_local_lib_bk && \
sudo cp /usr/local/lib/libboost* ./usr_local_lib_bk
```

The following files/folders are required for recovering
```
sudo rm -rf /usr/include/boost && \
sudo rm /usr/lib/x86_64-linux-gnu/libboost* && \
sudo rm -rf /usr/local/include/boost && \
sudo rm /usr/local/lib/libboost* && \

sudo mv usr_include_boost/boost /usr/include/ && \
sudo mv usr_lib_x86_64-linux-gnu/* /usr/lib/x86_64-linux-gnu/ && \
sudo mv usr_local_include_boost/boost /usr/local/include/ && \
sudo mv usr_local_lib/* /usr/local/lib/
```
