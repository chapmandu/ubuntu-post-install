Ubuntu Post Install Scripts
===========================

A semi-automatic and interactive set of post-installation scripts for Ubuntu and its derivatives. You can use this project to install your favourite apps, set your preferred settings, and do minor housekeeping.

## Organisation

This project is designed to be fairly modular (and not be one huge script) so you can easily delete or exclude bits/functions that you don't want to use.

 * [`data`](/data): files which are lists of packages<sup>&dagger;</sup> read by various functions.
 * [`functions`](/functions): the main functions of this scriptset. They should require little user-preference modification.
 * [`apps`](/functions/apps): functions for installing third-party applications. They are called in the [`install_thirdparty`](/functions/install_thirdparty) function.

*<sup>&dagger;</sup>These lists are preferential and should be updated with the packages you prefer*

## Adding Functions

Adding additional functions is as easy as editing one of the many already included functions and simply changing the variables. When you do add (or remove) functions be sure to update any main function (such as [`thirdparty`](/functions/thirdparty)) to reflect those changes.

## Usage

Run the bootstrapper:

`bash -c "$(curl -fsSL https://gist.githubusercontent.com/chapmandu/c10c1ebca14a90dc8c31ca05f724d1a9/raw/394ff2e00cc44886f355fa0f083dfd3a50af1d56/bootstrap.sh)"`

Once bootstrapped, you can just run the main script from the root of the source folder:

    ./ubuntu-post-install.sh
