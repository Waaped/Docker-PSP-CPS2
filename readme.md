Docker PSP CPS2 PSP.

Unfortunately you cannot run ROMCNV on mac without a VM, but docker is makes it easier and much more light weight.

you will need git, and docker preinstalled. Original built for MVS system, moded for CPS2


1. Open a terminal window

2. cd ~
3. Open .

Create file called ‘capcom’, paste all roms that you will be creating caches for.

  Back to terminal

3. git clone https://github.com/phoe-nix/NJEMU.git
(Launching container)
4. docker run --rm -it -v ~/NJEMU/romcnv:/root/romcnv -v ~/capcom:/root/capcom -w /root/romcnv debian:jessie bash
(Needed windows libraries)
5. apt-get update && apt-get install -y --no-install-recommends make automake gcc build-essential g++ cpp libc6-dev man-db autoconf pkg-config

6. make -f makefile.cps2 UNIX=1

7. ./romcnv_cps2 ~/capcom -all

8. mv cache ~/capcom

9. exit

Copy and paste cache files in to your PSP/GAME/CPS2/cache Directory
Copy and paste rom files in to your PSP/GAME/CPS2/roms

You are finished. 

