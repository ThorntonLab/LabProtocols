# Copying files from one machine to another

The `rsync` utility is the main way that we copy files to/from different computers.
It has the following key features:

* It can be told to only copy files on the source that are newer than, or do not exist on, the destination.
* It can be told to remove files from the destination that are not on the source.
* By default, it works via secure `ssh` protocols.

We will develop this page further in the future.
This program is a beast with a huge number of options.
You do also need to be a bit careful with these options!
For example, you may not always want the "remove from destination" option mentioned above, and you probably need to consider that on a case by case basis.

