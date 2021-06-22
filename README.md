# Python Client

This is a Python protoclient for connecting to an Infinispan server via Hotrod.
Focus is easyness to:

* install
* use
* understand
* extend


## Requirements

* python3
* pip3

TODO fill in

On fedora 34

 
   sudo dnf install gcc      
   sudo dnf install cc                                               
   sudo dnf install swig                                             
   sudo dnf install install gcc-c++                                  
   sudo dnf install  gcc-c++                                         
   sudo dnf install python3-devel                                    
   sudo dnf install protobuf-devel protobuf
   sudo dnf install cyrus-sasl-devel




## Generate the client

It should be as easy as type:

    pip3 wheel .

or (if you need to point your OPENSSL root dir)

    OPENSSL_ROOT_DIR=/usr/local/opt/openssl
    
## Install the client

    sudo pip3 install *.whl

## Use the client
An example of client usage is in the test.py script. Run it to check if everything
went fine. You need an up and running local Infinispan server ore you'll get a
connection error.

    python3 test.py

The C++ native libraries are placed by the installation script in `/usr/local/lib` directory (or in `$HOME/.local/lib` if installed
with --user), so you probably need to help the runtime loader.

    LD_LIBRARY_PATH=/usr/local/lib python3 test.py


## Uninstall

    sudo pip3 uninstall infinispan
