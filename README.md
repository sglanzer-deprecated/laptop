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
curl --remote-name https://raw.githubusercontent.com/sglanzer/laptop/master/laptop
```

Execute the downloaded script:

```sh
sh laptop 2>&1 | tee ~/laptop.log
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

OSX packaging:

* [Homebrew] for managing OSX libraries

[Homebrew]: http://brew.sh/

Terminal + Shell:

* [iTerm2] for a better terminal
* [Tmux] for saving project state and switching between projects

[iTerm2]: https://www.iterm2.com/
[Tmux]: http://tmux.github.io/

* [Zsh] as the shell
* [Prezto] amps up Zsh
* [Zsh-completions] additional completion definitions for Zsh

[Zsh]: http://www.zsh.org/
[Prezto]: https://github.com/sorin-ionescu/prezto
[Zsh-completions]: https://github.com/zsh-users/zsh-completions

OSX development tools:

* [X-Code] general development environment libraries

[X-Code]: https://developer.apple.com/xcode/

Unix tools:

* [OpenSSL] for Transport Layer Security (TLS)
* [The Silver Searcher] for finding things in files
* [Universal Ctags] for indexing files for vim tab completion
* [Watchman] for watching for filesystem events
* [Wget] for http(s)/ftp file retrieval

[OpenSSL]: https://www.openssl.org/
[The Silver Searcher]: https://github.com/ggreer/the_silver_searcher
[Universal Ctags]: https://ctags.io/
[Watchman]: https://facebook.github.io/watchman/
[Wget]: https://www.gnu.org/software/wget/

Git tools:

* [Git] for version control
* [GitHub Desktop] for working with Github repos
* [Hub] for interacting with the GitHub API
* [SourceTree] as an alternative to Github Desktop

[Git]: https://git-scm.com/
[GitHub Desktop]: https://desktop.github.com/
[Hub]: http://hub.github.com/
[SourceTree]: https://www.sourcetreeapp.com/

Server-side development:

* [Python] in support of Ansible
* [Virtualenv] to create isolated Python environments
* [Ansible] for deployment automation

* [Go] for microservice project development
* [Delve] to debug Go projects

* [Protobuf] data interchange format for gRPC

* [Gcloud SDK] CLI for interacting with Google Cloud

[Python]: https://www.python.org/
[Virtualenv]: https://virtualenv.pypa.io/en/stable/
[Ansible]: https://www.ansible.com/

[Go]: https://golang.org/
[Delve]: https://github.com/derekparker/delve

[Protobuf]: https://github.com/google/protobuf

[Gcloud SDK]: https://cloud.google.com/sdk/gcloud/

Client-side development:

* [N] for managing and installing Node.js versions
* [Node.js] (8.x) for running apps

* [Yarn] for managing JavaScript packages

* [ember-cli] (2.15.x) for managing Ember.js projects

[ember-cli]: https://ember-cli.com/
[N]: https://github.com/tj/n
[Node.js]: http://nodejs.org/
[NPM]: https://www.npmjs.org/
[Yarn]: https://yarnpkg.com/en/

IDEs:

* [VSC] for Go / Ember projects

[VSC]: https://code.visualstudio.com/

IDE extensions:

* ...more
* [vsc-ember-modules]: Ember module import snippets

[vsc-ember-modules]: https://github.com/sglanzer/vsc-ember-modules/blob/master/README.md

Image tools:

* [ImageMagick] for cropping and resizing images

[ImageMagick]: http://www.imagemagick.org/

Customize in `~/.laptop.local`
------------------------------

Your `~/.laptop.local` is run at the end of the Laptop script.
Put your customizations there.
See the [Thoughbot guide](https://github.com/thoughtbot/laptop#customize-in-laptoplocal) for an example.
