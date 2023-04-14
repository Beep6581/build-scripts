# build-scripts

These shell scripts are designed to simplify the process of compiling programs from source code on Unix-like systems

## Introduction

These shell scripts are designed to offer the fastest and most fool-proof path to compiling the respective programs from source, using the compilation options recommended by each program's developers. As such, they rely on optimal defaults and don't confuse the user with arcane options. They should "just work" out of the box.

It is up to you to ensure that your operating system has all the required dependencies installed for each respective program before attempting to compile it. The build scripts do not and will not handle dependencies, because doing so always ends up in bloated and obsolete scripts. To find which dependencies a given program requires, simply head over to that program's website or source code repository and look for the keywords "dependencies", "requirements" or "compilation" in the documentation. Typically you will find this information in the `README` or `INSTALL` text files. In most cases you will want to install these dependencies using your distribution's package manager.

## Usage

1. Download the script(s).
   - Either download all scripts by cloning the whole repository:
     ```
     git clone git@github.com:Beep6581/build-scripts.git
     ```
   - Or download a single script using `curl`:
     1. Click on the file you want to download here on GitHub.
     1. Click the "Raw" button.
     1. Copy the URL.
     1. Then, open your terminal and use the following command, replacing `URL_OF_RAW_FILE` with the URL you copied:
        ```
        curl -O URL_OF_RAW_FILE
        ```
1. Make the script(s) executable:
   ```
   chmod +x build-*
   ```
1. Run the relevant script to build the program, e.g. to build RawTherapee:
   ```
   ./build-rawtherapee
   ```
   Each script supports optional parameters, use the `-h` flag to find out more:
   ```
   ./build-rawtherapee -h
   ```

The script will tell you how to run the compiled program once it has completed running.

## Uninstallation

The source code of the program a script is designed to compile is typically cloned to `~/programs/code-foo` and the compiled program is typically placed in `~/programs/foo`, so removal is as simple as deleting those folders.

## Troubleshooting

If compilation fails, scroll through the wall of text and look for the keywords "fail", "error" or "abort". Typically they will appear in a striking color different from the rest of the log. The accompanying information will provide strong clues as to where the problem lies. Double-check that you have installed all of the dependencies. If you feel the problem lies in the source code and not with your setup, seek help on the respective project's forum or open an issue in their bug tracker.

## Updating

If you cloned the whole repository, you can update to the latest changes by issuing this command:
```
cd build-scripts
git pull
```
