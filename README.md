# brew-php

This project is a [Homebrew external command] that simplifies the process of
managing multiple PHP versions installed via Homebrew. Essentially all it does
is:

1. Unlink the current version of PHP
2. *Perform the requested action*
3. Re-link PHP (except when using `brew php link`)

Where the "requested action" can be:

- Installing packages
- Upgrading packages (including system-wide upgrades)
- Linking a different version of PHP

Also included are some informational commands to show the currently linked PHP
version, and list available PHP versions.

## Installation

    brew tap ezzatron/brew-php
    brew install brew-php

## Usage

```
brew php
    Manage multiple PHP installations

    brew php help
    Outputs this usage information

    brew php install [...]
    Unlink the current PHP package, install a package, then restore the linked PHP package

    brew php installed
    Output the currently installed PHP packages

    brew php link package
    Unlink the current PHP package, then link the requested package

    brew php linked
    Output the currently linked PHP package

    brew php upgrade [...]
    Unlink the current PHP package, perform an upgrade, then restore the linked PHP package
```

[homebrew external command]: https://docs.brew.sh/External-Commands
