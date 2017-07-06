# Docker Image to compile NSIS scripts

**Please note the purpose of this container is to aid in compiling NSIS scripts and not running the installers themselves**

[NSIS's homepage](http://nsis.sourceforge.net/Main_Page) explains best what it can do!:

> NSIS (Nullsoft Scriptable Install System) is a professional open source system to create Windows installers. It is designed to be as small and flexible as possible and is therefore very suitable for internet distribution.
>
> Being a user's first experience with your product, a stable and reliable installer is an important component of successful software. With NSIS you can create such installers that are capable of doing everything that is needed to setup your software.
>
> NSIS is script-based and allows you to create the logic to handle even the most complex installation tasks. Many plug-ins and scripts are already available: you can create web installers, communicate with Windows and other software components, install or update shared components and more.


---------------

### Features
- Meant to compile NSIS scripts
- Uses Debian experimental as it's the only Debian branch that has NSIS version 3 package.
- Has the `NSIS 3.01-1` package installed.
- Entrypoint is `makensis -V4`, therefore logging is enabled by default.

---------------

### docker run example

```
docker run -it \
    -v /path/to/project/on/host:/path/to/project/on/container \
    hp41/nsis:3.01-1 \
    /path/to/project/on/container/installer.nsi
```

---------------

### Possible modifications

- `ENTRYPOINT` can be modified in command/compose to run a command of your choice.