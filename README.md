# sage2-setup
 docker build --tag=sage2_custom .


docker create -v /sage2/config --name sage2Config sage2/master
docker create -v /sage2/keys --name sage2Keys sage2/master
docker create -v /root/Documents/SAGE2_Media --name sage2Uploads sage2/master


docker run --rm -it --volumes-from sage2Keys sage2/master /sage2/keys/GO-docker _.evl.uic.edu




docker run --rm -it -v $HOME/gitrepos/sage2-setup/seawall:/sage2/seawall --volumes-from sage2Config sage2/master  /bin/bash 