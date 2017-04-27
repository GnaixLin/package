# package
php- extension:phalcon for openwrt

#1 git clone
#2 copy to openwrt dir' feeds/packages/lang/ where you can find directory name 'php5'.the tree:
php5
|-- files
|-- Makefile
|-- patches
php5-phalcon
|-- Makefile

#3 and run 
scripts/feeds update -i packages 
to update links

then install with:
scripts/feeds install php5-pecl-phalcon

fi,compile it with:
make package/feeds/packages/php5-phalcon/compile V=99

