### Tutoriais sobre asdf

> **Fonte**: [using-asdf](https://gist.github.com/philiph/5bc52d744ffd6a8869393e2b41718262)

Note: this assumes you are using ZSH shell.

## Installation

Install [asdf](https://github.com/asdf-vm/asdf):
```
$ git clone https://github.com/asdf-vm/asdf.git ~/.asdf --branch v0.4.0
$ echo -e '\n. $HOME/.asdf/asdf.sh' >> ~/.zshrc
$ echo -e '\n. $HOME/.asdf/completions/asdf.bash' >> ~/.zshrc
$ source ~/.zshrc
```

Use asdf to install Ruby (https://github.com/asdf-vm/asdf-ruby):
```
$ asdf plugin-add ruby https://github.com/asdf-vm/asdf-ruby.git
$ asdf list-all ruby
$ asdf install ruby 2.4.0
$ asdf install ruby 2.4.1
$ asdf install ruby 2.4.2
$ asdf global ruby 2.4.2
```

Use asdf to install Erlang (https://github.com/asdf-vm/asdf-erlang):
```
$ asdf plugin-add erlang https://github.com/asdf-vm/asdf-erlang
$ asdf list-all erlang
$ asdf install erlang 19.1
$ asdf global erlang 19.1
```

Use asdf to install Elixir (https://github.com/asdf-vm/asdf-elixir):
```
$ asdf plugin-add elixir https://github.com/asdf-vm/asdf-elixir.git
$ asdf list elixir
$ asdf list-all elixir
$ asdf install elixir 1.3.4
$ asdf install elixir 1.4.2
$ asdf install elixir 1.5.2
$ asdf global elixir 1.5.2
```

Use asdf to install Node.js (https://github.com/asdf-vm/asdf-nodejs):
```
$ asdf plugin-add nodejs https://github.com/asdf-vm/asdf-nodejs.git

# Imports Node.js release team's OpenPGP keys to main keyring
$ bash ~/.asdf/plugins/nodejs/bin/import-release-team-keyring

$ asdf list-all nodejs
$ asdf install nodejs 7.8.0
$ asdf global nodejs 7.8.0
```

Use asdf to install Postgresql (https://github.com/smashedtoatoms/asdf-postgres):
```
# check that gcc installed first
$ asdf plugin-add postgres https://github.com/smashedtoatoms/asdf-postgres.git
$ asdf install postgres 9.6.5
$ asdf global postgres 9.6.5
```

It said:
```
You can now start the database server using:

    /Users/phil/.asdf/installs/postgres/9.6.5/bin/pg_ctl -D /Users/phil/.asdf/installs/postgres/9.6.5/data -l logfile start
```

Use asdf to install Redis (https://github.com/smashedtoatoms/asdf-redis):
```
# check that gcc installed first
$ asdf plugin-add redis https://github.com/smashedtoatoms/asdf-redis.git
$ asdf install redis 3.2.6
$ asdf global redis 3.2.6
```

Note: assuming you have to work with projects that use other version files (e.g. `.ruby-version`, `.node-version`, or `.nvmrc`), then in `~/.asdfrc` add the line:
```
legacy_version_file = yes
```

## Usage

asdf normally uses a `.tool-versions` file in your project's working directory to specify what versions of each tool to use.

For example:

```
$ cd ~/src/envato/hosted-shopfront
$ asdf current
elixir 1.5.2 (set by /Users/phil/.tool-versions)
erlang 19.1 (set by /Users/phil/.tool-versions)
nodejs 7.7.4 (set by /Users/phil/src/envato/hosted-shopfront/.nvmrc)
postgres 9.6.5 (set by /Users/phil/.tool-versions)
redis 3.2.6 (set by /Users/phil/.tool-versions)
ruby 2.4.2 (set by /Users/phil/src/envato/hosted-shopfront/.ruby-version)
```

Here you can see that most of my tools are using the default/global version.  However it has picked up nodejs 7.7.4 from the local `.nvmrc` and ruby 2.4.2 from `.ruby-version` file.

If, hypothetically, I wanted to use a particular version of elixir, I would type:

```
$ asdf local elixir 1.4.2
```

This creates a local `.tool-versions` file with contents:

```
elixir 1.4.2
```

Now if I check current tool versions, it shows elixir 1.4.2:

```
$ asdf current
elixir 1.4.2 (set by /Users/phil/src/envato/hosted-shopfront/.tool-versions)
erlang 19.1 (set by /Users/phil/.tool-versions)
nodejs 7.7.4 (set by /Users/phil/src/envato/hosted-shopfront/.nvmrc)
postgres 9.6.5 (set by /Users/phil/.tool-versions)
redis 3.2.6 (set by /Users/phil/.tool-versions)
ruby 2.4.2 (set by /Users/phil/src/envato/hosted-shopfront/.ruby-version)
```
