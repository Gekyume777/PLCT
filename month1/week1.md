#修复了一个无法运行的debian镜像源
##recover content：
###//about makefile
42: #&& git checkout 8b8fbf8 this branch can't be checkout
82:@git clone --depth 1 https://github.com/sophgo/u-boot-2021.10 $(BUILDDIR)/u-boot //refresh github's location 
111/112：BOARD=cv181x orginal BOARD=mars new hub mars has been removed
128：@git clone -b sg200x-dev --depth 1 https://github.com/sophgo/opensbi.git $(BUILDDIR)/opensbi //refresh github's location
143：CHIP_ARCH=CV181X add CHIP_ARCH parameter define
158：@git clone -b sg200x-dev --depth 1 https://github.com/sophgo/fsbl $(BUILDDIR)/fsbl //refresh github's location
198：@curl -L -s https://sophgo.my-ho.st:8443/public-key.asc -o $(BUILDDIR)/public-key.asc //ad -L option
202：#@-rm $(addon-targets) wrong dependent sequence，relate file don't created

###//about patch
fsbl
1 change board_name

u-boot:
1 change board_name
2 recover patch 2line skew，parameter lose
3 recover 补丁3 base on orginal logic change code

###//else
use dockerfile built image
