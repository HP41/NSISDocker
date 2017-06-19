# Docker Image for NSIS 3.01

1. Uses Debian experimental as it's the only Debian branch that has NSIS version 3.
2. Has the NSIS 3.01-1 package installed.
3. Entrypoint is `makensis -V4`, therefore logging is enabled by default.
4. Best run by mounting the necessary project folder using `-v` and then calling `docker run` with the path to the `.nsi` file under the mounted project folder within the container like so: `docker run -it \-v /path/to/project/on/host:/path/to/project/on/container hp41/nsis:3.01-1 /path/to/project/on/container/installer.nsi`