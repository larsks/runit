This is a version of runit patched for use with docker.  If you set
`RUNIT_EXIT_ON_HALT=1` in the environment before running `runit`,
then pid 1 will simply exit after stage 3 rather than attempting to
reboot/halt the container.

E.g:

    docker run -e RUNIT_EXIT_ON_HALT=1 ...

