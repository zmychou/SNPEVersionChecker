# SNPEVersionChecker

> snpe-version-checker  
>    -h print help  
>    -i import SNPE version info  
>    -s show the output result  

 

### for example:

snpe-version-check -i snpe-1.26.0.343 (this is the path of snpe folder)

this tool will check and import all files' md5sum result under lib/ folder except lib/python folder.

save the info inside the tool or separate file.

format is similar  with the table of dlc info. for example:

 
|SNPE version|	VARIANT	|file name	|md5sum|  
| ------ | ------ | ------ | ---|
|snpe-1.26.0.343	|aarch64-android-clang6.0|	libSNPE_G.so	|xxxx|
snpe-1.26.0.343	|dsp|	libsnpe_dsp_v65_domains_v2_skel.so|	xxxx
 

after -i snpe-1.26.0.343, we get all libraries md5 of snpe-1.26.0.343.

we can use -i snpe-1.25.0.287 to append the new md5 file.

 

if use -s option.

the tool will search all SNPE related file from the device.

then show a new table.

NOTE: By default, tool assume that your lib are sit in /system/lib, /system/lib64, /vendor/lib and /vendor/lib64, 
you can also set the LD_LIBRARY_PATH and ADSP_LIBRARY_PATH to specify some other directory that host the libs

SNPE version|	VARIANT|	path	|md5sum
--|--|--|--
snpe-1.26.0.343|	aarch64-android-clang6.0	|/system/lib/libSNPE_G.so	|xxxx
unknown|	unknown	|/vendor/lib/adsp/rfs/libsnpe_dsp_v65_domains_v2_skel.so|	xxxx
