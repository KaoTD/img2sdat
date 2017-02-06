# img2sdat
Convert filesystem ext4 image (.img) into Android sparse data image (.dat)
# mt-tools
Multi-Tools for editing sdat, img, simg,...


## Requirements
This binary requires Python 2.7 or newer installed on your system.

It currently supports Windows x86/x64, Linux x86/x64 & arm/arm64 architectures.



## Usage
```
mt-tools <tools> [options]
```
- `<tools>` = tool supported by mt-tools
- `[options]` = tool options

tool supported by mt-tools:
- `mkbootimg`
- `unpackbootimg`
- `uncpio`
- `mkcpio`
- `sdat2img`
- `img2simg`
- `simg2simg`
- `minigzip`
- `slit_app`



```
img2sdat.py <system_img> [outdir] [version]
```
- `<system_img>` = input system image
- `[outdir]` = output directory (current directory by default)
- `[version]` = transfer list version number (1 - 5.0, 2 - 5.1, 3 - 6.0, 4 - 7.0, will be asked by default, more info on xda thread)



## Example
This is a simple example on a Linux system:
img2sdat input file is sparse image. If your image is raw image, you need to convert it to sparse image before use img2sdat. use the command bellow:

```
~$ ./mt-tools img2simg raw_system.img new_system.img
```

After run above command, there is a new image named `new_system.img`
  then run this command:

```â‰
~$ ./img2sdat.py new_system.img out 2
```
It will create files `system.new.dat`, `system.patch.dat`, `system.transfer.list` in directory `out`.



## Info
For more information about this binary, visit http://forum.xda-developers.com/android/software-hacking/how-to-conver-lollipop-dat-files-to-t2978952.
