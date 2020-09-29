# Terminal "multiplexers"

Remote work often presents you with the following problem:

* You log in.
* You start a long-running job.
* You get lunch.
* You come back and your laptop had gone to sleep, killing your connection and thus your job.

The solution to this problem is to run a "terminal multiplexer" before starting long-running jobs.
For the above example, you can get back to your remote shell by logging in again and connecting to your session!
It is like magic.
The industry standards here are [GNU screen](https://www.gnu.org/software/screen/screen.html) and [tmux](https://en.wikipedia.org/wiki/Tmux).
(There are others, too.
Feel free to look into them.
We can install them if you want to try them.)
The former is likely to be installed "everywhere" already.
KT prefers `tmux` because he finds the default colors a nice reminder that he's not in a "normal" shell.
Google for a tutorial on one or both of these tools.
Incorporating these into your remote work flows will definitely save you some frustration.

Some people default to [nohup](https://en.wikipedia.org/wiki/Nohup) instead of terminal multiplexers.
The multiplexers are a much more general solution and should be preferred.
You cannot `nohup` your `vim` session, for example.

