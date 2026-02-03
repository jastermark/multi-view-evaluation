FROM ubuntu:18.04

# Initialize the environment 
RUN apt-get update
RUN apt-get install -y libboost-all-dev
RUN apt-get install -y libeigen3-dev
RUN DEBIAN_FRONTEND=noninteractive apt-get -yq install libpcl-dev
RUN apt-get install -y cmake git

# Build the ETH3D binaries
RUN git clone https://github.com/ETH3D/multi-view-evaluation.git
RUN cd multi-view-evaluation; mkdir build; cd build; cmake ../. ; make;
