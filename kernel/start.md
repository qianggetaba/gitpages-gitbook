kernel entry point instruction: arch/x86/boot/header.S

    .globl	_start  ; not at the very begining
arch/x86/boot/setup.ld for the linker scipt, will arrange the seciton postion

init/main.c#start_kernel  is the kernel entry point, the arch folder is bootstrap for arch related stuff.

make -n > make_output.txt 2>&1  ; output make commands

after kernel compile, will generate file "*.o.cmd" contain the command that generate the *.o in each folder 

kernel makefile compile sequence:
- determine the arch
- do arch related makefile, arch/x86/Makefile, output vmlinux
- module compile
- compress vmlinux to bzImages
