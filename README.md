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

`Homebrew 3.4.11

Homebrew/homebrew-core (git revision 5bf515994a1; last commit 2022-05-11)`

