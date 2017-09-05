Laptop
======

Laptop is a script to set up an macOS laptop for web / mobile / server development.

It can be run multiple times on the same machine safely.
It installs, upgrades, or skips packages
based on what is already installed on the machine.

Credits
-------

This laptop script is based on
[thoughbot's laptop](https://github.com/thoughtbot/laptop) script and has
simply been customized to our needs.

Requirements
------------

Supported OS versions:

* macOS Sierra (10.12)

Older versions may work but aren't necessarily tested.

Install
-------

Download the script:

```sh
curl --remote-name https://raw.githubusercontent.com/sglanzer/laptop/master/mac
```

Execute the downloaded script:

```sh
sh mac 2>&1 | tee ~/laptop.log
```

Optionally, review the log:

```sh
less ~/laptop.log
```

Debugging
---------

Your last Laptop run will be saved to `~/laptop.log`.

What it sets up
---------------

macOS tools:

* [Homebrew] for managing operating system libraries
* [X-Code] to provide libraries for the general development environment

[Homebrew]: http://brew.sh/
[X-Code]: https://developer.apple.com/xcode/

Unix tools:

* [Exuberant Ctags] for indexing files for vim tab completion
* [Git] for version control
* [iTerm2] for a better terminal
* [OpenSSL] for Transport Layer Security (TLS)
* [Prezto] for Zsh configuration
* [Tmux] for saving project state and switching between projects
* [Watchman] for watching for filesystem events
* [Wget] for http(s)/ftp file retrieval
* [Zsh] as your shell
* [Zsh-completions] additional completion definitions for Zsh

[Exuberant Ctags]: http://ctags.sourceforge.net/
[Git]: https://git-scm.com/
[iTerm2]: https://www.iterm2.com/
[OpenSSL]: https://www.openssl.org/
[Prezto]: https://github.com/sorin-ionescu/prezto
[Tmux]: http://tmux.github.io/
[Watchman]: https://facebook.github.io/watchman/
[Wget]: https://www.gnu.org/software/wget/
[Zsh]: http://www.zsh.org/
[Zsh-completions]: https://github.com/zsh-users/zsh-completions

GitHub tools:

* [Hub] for interacting with the GitHub API

[Hub]: http://hub.github.com/

Image tools:

* [ImageMagick] for cropping and resizing images

[ImageMagick]: http://www.imagemagick.org/

Programming languages, package managers, and configuration:

* [Ansible] for deployment automation
* [Delve] to debug Go projects
* [ember-cli] for managing Ember.js projects
* [Go] for microservice project development
* [Node.js] and [NPM], for running apps and installing JavaScript packages
* [NVM] for managing Node.js versions
* [Python] in support of Ansible
* [Protobuf] data interchange format for gRPC
* [Virtualenv] to create isolated Python environments
* [Yarn] for managing JavaScript packages

[Ansible]: https://www.ansible.com/
[Delve]: https://github.com/derekparker/delve
[ember-cli]: https://ember-cli.com/
[Go]: https://golang.org/
[Node.js]: http://nodejs.org/
[NPM]: https://www.npmjs.org/
[NVM]: https://github.com/creationix/nvm
[Protobuf]: https://github.com/google/protobuf
[Python]: https://www.python.org/
[Virtualenv]: https://virtualenv.pypa.io/en/stable/
[Yarn]: https://yarnpkg.com/en/

IDEs:

* [VSC] for Go / Ember projects

[VSC]: https://code.visualstudio.com/

Customize in `~/.laptop.local`
------------------------------

Your `~/.laptop.local` is run at the end of the Laptop script.
Put your customizations there.
See the [Thoughbot guide](https://github.com/thoughtbot/laptop#customize-in-laptoplocal) for an example.

Development
------------

Edit the `mac` file.
Document in the `README.md` file.
Follow shell style guidelines by using [ShellCheck] and [Syntastic].

```sh
brew install shellcheck
```

[ShellCheck]: http://www.shellcheck.net/about.html
[Syntastic]: https://github.com/scrooloose/syntastic
