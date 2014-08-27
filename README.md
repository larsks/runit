This is a version of runit patched such that running `runit-init x`
will cause pid 1 to exit, rather than trying to reboot/halt the
system.

This was originally intended for use with docker, but is probably the
wrong solution.  You probably want [this branch][] instead.

[this branch]: https://github.com/larsks/runit/tree/feature/exit-via-env
