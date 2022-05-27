# MAC M1 Installation

If you are using new mac m1/m1 pro/m1 pro max then you can follow this installation process.

The first thing you should install is `Brew`

## Install Brew

To install brew first run the following command in the terminal:

`/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`

This will take few minutes depending on your internet connext. If successfully installed the you can notice that it's asking to run the following command:

`echo 'eval $(/opt/homebrew/bin/brew shellenv)' >> ~/.zprofile
eval $(/opt/homebrew/bin/brew shellenv)`

Next check if your brew installed properly. Use following command to check it:

`brew --version`

You should see a message like this:

`Homebrew 3.4.11`

`Homebrew/homebrew-core (git revision 5bf515994a1; last commit 2022-05-11)`

## Install Python3 via brew

First check what version of python is running in you mac with the following command.

`python -V`

you should see something like this:

`Python 2.7.18`

Note that this is python 2 so if you also have python3 pre-installed in you mac. Just type the following command to check that:

`python3 -V`

you should see something like this:

`Python 3.8.9`

Now check where is you python3 installed using:

`which -a python3`

You should see:

1)

`/usr/bin/python3`

or,

2)
`/opt/homebrew/bin/python3
/usr/bin/python3`

If you see 1, then your python was not installed using bre. Hence, managing the packages and versions will be confusing. To install python via brew use the following command:

`brew install python`

Once successfully installed you should be able to see 2, if you type `which -a python3`.

However, your default python path is `/usr/bin/python3` so to change that run the following command.

`hash -r
type python3`

Now you will notice that your python3 path is changed to:

`python3 is /opt/homebrew/bin/python3`

Also notice your pip3 path also changed.

[Check for more details](!https://github.com/Homebrew/discussions/discussions/476)

## Install Java using Azul Zulu

Installing java and jdk in new mac m1 os can be can be troublesome. The easiest way to install it is by using Azul zulu. Go to [Azul Zulu](!https://www.azul.com/downloads/?version=java-8-lts&os=macos&package=jdk#download-openjdk) and download the .dmg file for ARM 64 bit. Simply install it and after it is done check if java installed successfully by using:

`java -version`

you should see something like:
`openjdk version "1.8.0_332"`

`OpenJDK Runtime Environment (Zulu 8.62.0.19-CA-macos-aarch64) (build 1.8.0_332-b09)`

`OpenJDK 64-Bit Server VM (Zulu 8.62.0.19-CA-macos-aarch64) (build 25.332-b09, mixed mode)`
