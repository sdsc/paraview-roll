# SDSC "paraview" roll

The paraview-roll is deprecated; SDSC no longer supports or develops it.

## Overview

This roll bundles the ParaView data analysis and visualization package.

For more information about ParaView please visit the official web page:

- <a href="http://www.paraview.org" target="_blank">ParaView</a> is an
open-source, multi-platform data analysis and visualization application.
ParaView users can quickly build visualizations to analyze their data using
qualitative and quantitative techniques.


## Requirements

To build/install this roll you must have root access to a Rocks development
machine (e.g., a frontend or development appliance).

If your Rocks development machine does *not* have Internet access you must
download the appropriate paraview source file(s) using a machine that does
have Internet access and copy them into the `src/<package>` directories on your
Rocks development machine.


## Dependencies

Unknown at this time.


## Building

To build the paraview-roll, execute these instructions on a Rocks development
machine (e.g., a frontend or development appliance):

```shell
% make default 2>&1 | tee build.log
% grep "RPM build error" build.log
```

If nothing is returned from the grep command then the roll should have been
created as... `paraview-*.iso`. If you built the roll on a Rocks frontend then
proceed to the installation step. If you built the roll on a Rocks development
appliance you need to copy the roll to your Rocks frontend before continuing
with installation.


## Installation

To install, execute these instructions on a Rocks frontend:

```shell
% rocks add roll *.iso
% rocks enable roll paraview
% cd /export/rocks/install
% rocks create distro
% rocks run roll paraview | bash
```

In addition to the software itself, the roll installs paraview environment
module files in:

```shell
/opt/modulefiles/applications/paraview
```
