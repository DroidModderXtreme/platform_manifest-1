INITIALIZING REPOSITORY
=======================

Init core trees without any device/kernel/vendor :

    $ repo init -u https://github.com/Gava97/platform_manifest-1.git -b kitkat

Init repo with all devices, kernels and vendors supported by AOKP :

    $ repo init -u https://github.com/AOKP/platform_manifest.git -b kitkat -g all,kernel,device,vendor

Init repo only for a particular device :

    $ repo init -u https://github.com/AOKP/platform_manifest.git -b kitkat -g all,-notdefault,<devicename>,<vendorname>

for example, to init only trees needed to build mako :

    $ repo init -u https://github.com/AOKP/platform_manifest.git -b kitkat -g all,-notdefault,mako,lge

Init repo for multiple devices :

    $ repo init -u https://github.com/AOKP/platform_manifest.git -b kitkat -g all,-notdefault,<devicename1>,<devicename2>,<devicename3>,<vendorname1>,<vendorname2>,<vendorname3>

for example, to init trees needed to build mako and flo :

    $ repo init -u https://github.com/AOKP/platform_manifest.git -b kitkat -g all,-notdefault,mako,flo,lge,asus


sync repo :

    $ repo sync
