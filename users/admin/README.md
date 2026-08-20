/users/$USER

# User Home

SFH homes are different from FHS homes in some ways and similar in others. What makes SFH homes unique is that nothing is hidden by default; in fact, SFH discourages hiding folders or files at all, as that would be antithetical to the priority of demystifying the machine.

Furthering that demystification, SFH prioritizes a practically 1-to-1 relationship between the filesystem root and user homes—in areas that make sense and aid predictability. For example: if users need their own, isolated version of a program instead of the one available system-wide, or if they do not have the necessary permissions to install a system-wide program, they can install it to `~/software/{programs,libraries}` instead of `/software/{programs,libraries}`. User-specific credentials like SSH keys go in `~/credentials` instead of `/credentials`. I think you get the picture. 

The only caveat to this is the disparity between `/settings` and `~/preferences`, but it should be noted this was a conscious design choice. `/settings` is intended to define system-wide defaults for the root account and new users, whereas `~/preferences` defines per-user behaviors that diverge from the defaults; it is for how users *want* things to act rather than how they act on their own.

SFH user homes also reimagine the `~/Desktop` folder and release control of user data folders like `~/Pictures` and `~/Documents` to the user entirely. To better reflect modern workflows, `~/Desktop` is now `~/canvas`—your active worksurface where you keep things you need to remember to do something with. Driven by that same philosophy, it is also the defaut dumping ground for browser downloads, reminding you they exist until you delete them or file them appropriately.

Folders like `~/Documents`, `~/Pictures`, etc. etc. are not strictly defined by the SFH as it does not assume what kind of data users will be storing on their machine. It is much less annoying for users to create one or two directories that weren't there than it is for them fight an operating system constantly creating ones they never asked for and won't use. My offical recommendation, and what I personally do, is to create an `~/archive` folder or something similar where you structure your own data storage as you see fit.
