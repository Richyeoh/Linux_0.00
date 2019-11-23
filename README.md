# Linux_0.00
Rewrite Linux 0.00 with NASM

## Need dependence

nasm & virtual machine

## How to generate image

```sh
 nasm boot.asm -o boot.bin
 nasm head.asm -o head.bin
 dd if=/dev/zero of=boot.img bs=512 count=2880
 dd if=boot.bin of=boot.img bs=512 conv=notrunc
 dd if=head.bin of=boot.img bs=512 seek=1 conv=notrunc
```
