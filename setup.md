## CentOS

	sudo yum install m4 openssl-devel db4-devel libdb-cxx-devel boost-devel protobuf-devel git
	
## Build the Gcoin

	./autogen.sh --without-gui --without-miniupnpc
	./configure
	make
	
## Running
Place a configuration file in `~/.gcoin/gcoin.conf` with the following contents (You don't need to modify anything)
     
     addnode=140.112.29.201:12321
     addnode=54.254.159.145
     rpcuser=username
     rpcpassword=password

## Env
in `.bashrc`

	 export LD_LIBRARY_PATH=/usr/local/ssl/lib
	 export LDFLAGS=-L/usr/local/ssl/lib
	 export CFLAGS=-I/usr/local/ssl/include
     
## DONE