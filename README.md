UltimaAOSP 4.4.4 for i9300 and i9505
====================================

Download:
----------
* mkdir ~/UltimaAOSP
* cd ~/UltimaAOSP
* repo init -u git://github.com/UltimaAOSP/platform_manifest -b kk-4.4
* repo sync


Building:
----------
* . build/envsetup.sh
* lunch (ignore 1 & 2, choose 3, 4, 5 or 6)
* make otapackage -j4 (replace 4 with as many cores there are on your CPU)

(after doing 'make clean' you need to lunch again before rebuilding)



Fixing 'lz4c' not found:
------------------------

Due to new lossless kernel compression (LZ4), the lz4c binary is needed until properly implemented in the rom tree. This can be installed by following the steps below:

- wget http://lz4.googlecode.com/files/lz4-r112.tar.gz
- tar -xf lz4-r112.tar.gz
- cd lz4-r112
- make
- sudo make install
