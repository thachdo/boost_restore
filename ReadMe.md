### Recover to boost 1.65 (ubunbu 18.04) after installing a newer boost version
The following files/folders are required for the recovery
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
