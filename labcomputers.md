## Lab computers

### Setting up Pop OS on lab machines

#### Use LTS releases

Using `LTS` releases is critical.
The 6 month "developer" releases can suffer from user interface lag due to the NVIDIA drivers.
We have had issues with key commands taking over one second to register in the GNOME terminal.
We have had the `nouveau` drivers freeze up on us.
We've seen this with multiple different card of various ages.
These issues all go away (knock on wood...) with the `LTS` releases.

An no, "force full composition" (in the NVIDIA X server settings) doesn't fully solve these problems.

The procedure is simple:

* Download `LTS` release and flash it to a `USB` drive.
* Reboot and install.
* Use the advanced install options to custom partition the drives if needed.

It is possible that the boot device order will need to be adjusted in the machine's `BIOS`!

Prior to such an install, it is prudent to:

* Back up `/home` to one of the secondary drives.
  To do so, use `rsync -avr`.

#### NVIDIA GPU setup

This section is current with `20.04`.

This is very straightforward:

```sh
sudo apt install system76-cudnn-11.1 libcusolver* python3-pip
pip3 install tensorflow-gpu
```

Then,

```py
python3
import tensorflow as tf
tf.config.list_physical_devices('GPU') 
```

The information printed to screen should tell you that the GPU have been found and "registered".

### AMD GPU setup

`TBD`--waiting for 6700xt to become available!
