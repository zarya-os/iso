### iso

This ISO builder was basically a combination of previous efforts from Ubuntu
Budgie (budgie-remix at the time), some stuff from livecd-rootfs from launchpad
and Elementary OS, thanks to the amazing devs from all around!
Elem Link: https://github.com/elementary/os

### building locally

The following example uses Docker and assumes you have Docker correctly installed and set up:

 1) Clone this project & `cd` into it:

    ```bash
    git clone https://github.com/zarya-os/iso && cd iso
    ```

 2) Run the build:

    ```bash
    docker run --privileged -i -v /proc:/proc \
        -v ${PWD}:/working_dir \
        -w /working_dir \
        debian:latest \
        /bin/bash -s etc/terraform.conf < build.sh
    ```

 3) When done, your image will be in the `builds` folder.
