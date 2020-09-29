# "Logging in" to a remote server

To "log in" to a remote machine means that you wish to obtain an interactive shell on another machine.
The primary command line tool for such remote shells is `ssh`:

```sh
ssh username@machine
```

For example:

```sh
ssh kevin@labmachine.bio.uci.edu
```

You will need to enter your password.
If your your remote work will require interaction with graphical tools, then you need to enable `X11` forwarding:

```sh
ssh -Y username@machine
```

See the `man` page for `ssh` for more details about `X11` forwarding.

### VPN

If you are working from off-campus, then you'll need to enable your [VPN](vpn) first.

### Password-free ssh

One can exchange encrypted "keys" between machines in order to avoid having to enter passwords.
Google "password free ssh" and read one or more of the zillions of how-to pages.
Many people like the convenience of this approach.
You need to do it for all to/from connections, or at least the most common ones.
For example, setting it up between a lab desktop and the campus cluster means you still need a password when connecting from your laptop at home to the cluster.

I will state that I *do not* do this in general.
Imagine that your desktop account is compromised.
The "hacker" now has free access to all of your files on all remote servers where you've exchanged keys!
(This access is also true if you use the same password for all machines.)
It is easy for an intruder to discover what other machines you connect to.
For example, they can peruse your shell command history.

A more advanced, and safer, method involves protecting all of your exchanged `ssh` keys with a global (and unique) password.
See [here](https://opensource.com/article/19/4/gpg-subkeys-ssh) for example.
This advanced method can be coupled with hardware-based two-factor authentication.
I may explore this option for the lab in the future.

