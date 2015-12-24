git remote add ubuntu git://git.debian.org/~lamont/util-linux.git
git fetch ubuntu
git checkout -b ubuntu remotes/ubuntu/master
git checkout master
git merge ubuntu
git remote add vanilla git://git.kernel.org/pub/scm/utils/util-linux/util-linux.git
git fetch dmesg
git checkout -b master-vanilla remotes/vanilla/master
git checkout master
git merge master-vanilla


resolv conflict and then 
./autogen.sh
./configure
./make

dmesg -V

