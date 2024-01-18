---
title: ABLeS - Application Installation Guidelines
---

# Introduction

The following documentation describes the installation procedures for bioinformatics software at the National Computational Infrastructure (NCI project allocation if89) enabled by the Australian BioCommons and included in Tools and Workflows repository.

The maintenance process is purposely standardised using scripts to allow for sustainability. These scripts were developed to be similar to the NCI software management scripts to enable transferability. NCI staff, AusARG bioinformatics participant, and bioinformatics/computational biology leads for the Australian BioCommons Leadership Share (ABLeS) program contributed to these scripts.

>* All software on if89 should be installed into `/g/data/if89/apps directory`. 
>* One directory for each software, then a subdirectory for each version of this software. 
>* At the end, the path for a tool’s version is `/g/data/if89/apps/<package>/<version>`.

For each software, a Unix module file (in TCL) is created to be loaded when the software is used. 
This module file should also load all of the software's dependencies. 
For each software, an installation script should be created to install the software whenever needed. 
This helps to automate the process when a reinstallation is required. 
This script should be added to the repository of all scripts and patches, which is available at: [https://git.nci.org.au/dsr900/ables-software-installations](https://git.nci.org.au/dsr900/ables-software-installations). This script repository follows the same file structure as the NCI `/apps` directory which is `/<package>/<version>`.

# Prerequisites
In order to contribute to `if89`, you need to satisfy the following conditions:

1. **Obtain access to the `if89` project**: Everyone can request access to `if89` if they have a user account on GADI. Simply, request to join at this [link](https://my.nci.org.au/mancini/project/if89).
2. **Request to join the writer participant under `if89`**: request to join at this [link](https://my.nci.org.au/mancini/project/if89_w)
3. **Request access to `ables-software-installations` repository**: The repository link is [https://git.nci.org.au/dsr900/ables-software-installations](https://git.nci.org.au/dsr900/ables-software-installations). Access is managed through your Gadi username and password.
   
   If you do not have access, please contact one of the following repository maintainers and they will add you:
      * Ziad Al Bkhetan: <ziad@biocommons.org.au>
      * Javed Shaikh: <javed.shaikh@anu.edu.au>
   

# General Guidelines

These are some general guidelines to be aware of before installing any software:

1. If you have access to the source code, try to install the software from this source. 
2. This is the highest priority. More details on compiling from source code on GADI is available at this [link] (https://opus.nci.org.au/display/Help/Compiling+and+Linking).
3. If the package/software requires other tools to be installed, then each tool should be installed separately following the same procedure below.
4. All installation steps (i.e. make check or equivalent) should be completed within the installation script. 
5. When running the final installation, a script should fail if any command executed fails using the set `-e` flag. 
When the `--appbot` flag is appended to the install script, this setting is applied by the helper_functions.sh script. 
If a command is expected to fail, '`|| true`' should be appended to the command. 
This will cause the compound command to exit with a successful status, even if the command to the left of the `||` operator fails.
6. Any ‘hand-edits’ that are required to configure/build an application correctly (including fixes required to pass unit testing) must be submitted as patch files within the build sub-directory, 
and the corresponding patch command must be run by the install script. An example of this can be found in the `bwa/0.7.17` installation script in the repository.
7. For compiled applications, optimisations flags should be selected such that the application can run on any of the CPU architectures available on Gadi. 
The following flags are recommended for the Intel compilers:
`$ i{cc,cpc,fort} -xBROADWELL -axSKYLAKE-AVX512,CASCADELAKE ...`
This will create a ‘fat binary’ that contains optimised code for all listed architectures. The Intel runtime library can detect the architecture at runtime and select the correct optimised code to use. The GNU compiler does not have this capability, so one architecture must be selected at compile time as follows:
`$ g{cc,++,fortran} -march=broadwell ...`
8. Module and/or common files must also be created by the installation script.
 
# First-time installation procedure

Before installing any software, make sure the software is not already installed into `/g/data/if89/apps/` as well as into NCI supported apps `/apps/`.

We recommend checking out one installation, for example, the tool MMseqs2, version 13-4511:

install script: [https://git.nci.org.au/dsr900/ables-software-installations/-/tree/main/MMseqs2/13-45111](https://git.nci.org.au/dsr900/ables-software-installations/-/tree/main/MMseqs2/13-45111) 

installed app:  `/g/data/if89/apps/MMseqs2/13-45111/`

module file: `/g/data/if89/apps/modulefiles/MMseqs2/13-45111`


The procedure consists of three main stages:
1. Prepare an `install.sh` script that contains all installation steps
2. Install the software on the `if89` project
3. Add the installation script to the `ABLeS-software-repository`

**Details are below**

1. Clone `ables-software-installations` If you have done this step before, jump to step 2.
   If this is your first time adding to `if89`, you will need to clone the `ables-software-installations` repository from [https://git.nci.org.au/dsr900/ables-software-installations](https://git.nci.org.au/dsr900/ables-software-installations). Access is managed through your Gadi username and password.
   If you do not have access, please contact one of the following repository maintainers and they will add you:
      * Ziad Al Bkhetan: <ziad@biocommons.org.au>
      * Javed Shaikh: <javed.shaikh@anu.edu.au>
   
   There is no specific location to clone the repo into, however, we recommend using the home directory ($HOME). You can create a directory with your username there and use it for your testing. You can use the following commands for this purpose:
 
```
    mkdir $HOME/$USER
    cd $HOME/$USER
    git clone https://git.nci.org.au/dsr900/ables-software-installations.git
```

2. Make sure that the local repository is up to date before starting work on any new package. A branch must be created from the latest version of the ‘main’ branch of the repository. Change `APP_NAME` and `APP_VERSION` according to the software you are installing.

~~~
    cd $HOME/$USER/ables-software-installations
    git checkout main
    git pull
    # edit below
    export APP_NAME="APP_NAME"
    export APP_VERSION="APP_VERSION"
    git checkout -b ${APP_NAME}/${APP_VERSION}
~~~

3. Create a directory for the app and its version following the same file structure as other apps. 
Copy the install script template to the directory and rename it to install.sh. 
Make sure that the file is executable. 
The install template is available directly under the root directory of `ables-software-installations`. 
 
~~~
    mkdir -p ${APP_NAME}/${APP_VERSION}
    cd ${APP_NAME}/${APP_VERSION}
    cp ../../install.template ./install.sh
    chmod u+x ./install.sh
~~~

4. We recommend using other paths for testing as mentioned in the template file. You can use the same file paths mentioned there for testing until you are happy with the installation, then use the original paths. Details are in the template file.
5. Edit the install file according to the app you are installing according to the tips provided within the install template. 
6. Run the install.sh script to do the final installation. Make sure the paths are configured to contain the final values not the testing ones.

~~~
     ./install.sh
~~~

7. Make sure you clean up the directory
    * only install.* and installation related files if they exist should be kept) and only keep the installation files needed to be pushed to the repository. 
    * Then commit your changes (should be adding install.sh file) and merge the branch you created with the main branch. 
    * There is a chance that other people working on the repository push some changes to the repository after you create the branch. This will mean your local repository is not up to date when compared to the remote repository. In this case, you need to pull the repository to update the local repository before you push your changes.

  
~~~
    # clean up, rm *.log …
    cd $HOME/$USER/ables-software-installations
    git add .
    git commit -m "Adding ${APP_NAME}/${APP_VERSION}"
    git checkout main
    git merge ${APP_NAME}/${APP_VERSION}
    git push
 ~~~


# Modifying Existing Installations

* If an app installation needs to be altered after being made generally available, an update script needs to be added to the repository in the same directory as the installation script of the application being modified, and the same branch-merge procedure must be followed. 
* The update script should be named `update.*` and the same update script will not be run twice. It is recommended to give the update script a descriptive name e.g. `update.shortdescription.sh`. 
* The database of installations maintained by the installer tool will record the order in which update scripts were run, so in cases of disaster recovery, the current state of an application in the installation area will be able to be reconstructed by running `install.sh`, then all `update.*`  scripts in a given `<software>/<version>`  directory chronologically.

# When scripted installations are not possible

If scripted installations are not possible, sufficient documentation needs to be available such that the installation can be performed consistently by any `if89` maintainer.
Please contact ABLeS team if you have such case.

* The documentation can be placed in the install script, or on an wiki page within the apps installation repository. 
* A final tar file containing the completed installation should be placed in the appropriate subdirectory of `$SOURCE_DOWNLOADS_CACHE`. 
* An installation script is still required, however, all it needs to do is untar the completed installation from the staging area into `/g/data/if89/apps`. 
* Examples of acceptable manual installations are when GUI installers are required, or when pre-built software must be retrieved from behind an authenticated web service.

# Installation Script Standards

A few general rules need to be followed in order for the installation repository and python tool to work together cohesively. 
They are as follows:

* Use download_source instead of wget or curl to retrieve software source code.
* In the case of software that is retrieved from behind an authenticated web service, as much of the installation as possible must be scripted. For example, an application that is retrieved by a git clone that requires a key must have every step after the gitafter git clone performed by the installation script. 
* The script used to install an application must match the pattern install.*
* There must be only one file of that pattern in each sub-directory in the installation repository. 
* At the moment only bash (`.sh`) is supported.
* Installation scripts should not be run twice, any changes that are made after installation should be performed by a script that matches the pattern `update.*`
* Bash scripts run by the python wrapper are run with set `-e`, meaning any individual command that fails will cause the script to fail and therefore report a failed installation. Any commands that are intended to fail can be appended with `|| true`, which will allow the script to continue if the command fails.
* The build should be performed in a directory whose name appears in the .gitignore file and resides inside the appropriate package subdirectory. This makes clean-up after installation much simpler.
* Where ‘module load’ commands contain anything other than plain-text module names, it is strongly encouraged to use the `#APPBOT DEPENDS_ON` directive. The order of installations cannot be guaranteed unless all dependencies are known to the python installation tool.
* Use verify_and_run wherever possible, including wrapping of complex sequences of operations into bash functions. 
  + This prevents re-running command sequences in case of failure, and automatically generates log files. 
  + If the same functions are appearing repeatedly in multiple installation scripts, they can be added to the main helper_functions.sh script.
* Any software that is identified only by a date stamp should use `YYYYMMDD` format to allow version comparison extensions to work correctly.
* Avoid `<app>/<version>-<compiler>-<option>-<mpi>-...` type structures. A lot of this can be handled by the MPI/compiler hierarchies that can be created during application installations. Where multi-MPI/compiler installations are not possible, compatibility requirements should be enforced using modules extensions.

# Appendices

## The `helper_functions.sh` script

The `helper_functions.sh` script defines some useful variables and functions:

### Variables

* `$APPS_BASE`: The path to the top level applications installation directory (`/g/data/if89/apps`). Use this to specify paths to installation directories instead of `/g/data/if89/apps` directly
* `$MODULE_BASE`: The path to the top level directory containing module files. (`/g/data/if89/apps/modulefiles`). Use this to specify the location of module files instead of using `/g/data/if89/apps/modulefiles` directly.
* `$INTERACTIVE_MODE`: When the installation script is in development and testing, this is set to 1, when the installation script is run for the final installation, this is set to 0. Use this to modify the behaviour of the script during the final installation (e.g. skipping make check steps that have already been proven to succeed).
* `$TOPDIR`: The directory in which the installation was started, usually `<app-installs-repo-local-copy>/${APP_NAME}/${APP_VERSION}`
* `$REPO_TOPDIR`: The path to the top-level directory of your working copy of the `ables-software-installations` repository.
* `$SOURCE_DOWNLOADS_CACHE`: A shared directory into which files downloaded using `download_source`  are placed. Can be referenced directly when staging components of installations that cannot be automated (e.g. GUI installers, authenticated git clone, etc).

### Functions

* `verify_and_run <command>`: Prompts the user before running <command>. Creates an automatically named log file for the command, and a checkpoint file if the command finishes successfully. Will not run `<command>` if the checkpoint file is present. Designed to be used during manual test installations to verify that installation steps have run correctly. When run during automatic installs, this function creates a log file and checkpoint file but does not create a prompt.

* `download_source <url> <app_name> <app_version>`: Download the file from `<url>` to the directory `${SOURCE_DOWNLOADS_CACHE}/<app_name>/<app_version>` for archiving (this copy should not be used in the installation). Download_source will then copy the downloaded file to the working directory which can download It also keeps a copy in the working directory which can be used for the remaining part of the installation instead of using the downloaded file in `${SOURCE_DOWNLOADS_CACHE}`. This function should be used in preference to curl  or wget  when retrieving source code, as it saves files to a shared area where they can be retrieved later without internet access. This helps ensure reproducibility, as it guards against externally sourced files changing or being removed from the web entirely.


# Contributors to this documentation:

* **Dale Roberts** *(NCI)*
* **Johan Gustafsson** *(Australian BioCommons, University of Melbourne)*
* **Ziad Al Bkhetan** *(Australian BioCommons, University of Melbourne)*
* **Hardip Patel** *(The John Curtin School of Medical Research, Australian National University)*
