﻿#tecnoyucas.github.io

Yucazos de Innovación Tecnológica

## Installation in Ubuntu

### Ruby, gems, jekyll

```bash
  apt-get install ruby1.9.1-dev

  gem install jekyll
```
## Running

```bash
  jekyll serve
```

## Installation in Windows

### Ruby, gems, jekyll
1 - Install the Ruby from http://rubyinstaller.org/downloads/ and install it to path such as C:\ruby

2 - Download “DEVELOPMENT KIT” installer that matches the Windows architecture and the Ruby version just installed. For example, DevKit-tdm-32-4.5.2-20111229-1559-sfx.exe is for use with Ruby 1.8.7 and 1.9.3. Install the Ruby development kit from the same location above and extract it to path such as c:\devkit.

Run the following command to generate the config.yml file to be used later

```bash
ruby dk.rb init
```

3 - Edit the generated config.yml file to include installed Rubies. For example, in our case, it will look like this

```bash
# This configuration file contains the absolute path locations of all
# installed Rubies to be enhanced to work with the DevKit. This config
# file is generated by the 'ruby dk.rb init' step and may be modified
# before running the 'ruby dk.rb install' step. To include any installed
# Rubies that were not automagically discovered, simply add a line below
# the triple hyphens with the absolute path to the Ruby root directory.
#
# Example:
#
# ---
# - C:/ruby19trunk
# - C:/ruby192dev
#
---
- C:/ruby
```

4 - Run the following command to install to DevKit enhance your installed Rubies. This step installs (or updates) an operating_system.rb file into the relevant directory needed to implement a RubyGems
```bash
ruby dk.rb install
```

5 - Install Jekyll using following command, install jekyll ver. 1.4.2 
```bash
gem install jekyll --version "=1.4.2"
```
6 - Now we need to install python, can be downloaded from http://www.python.org/download/ (Python 2.7.6 Windows Installer).

7 - Now we need to install easy_install. This can be installed from http://pypi.python.org/pypi/distribute Download ez_setup.py and run the file.

8 - Now to install pygments, simply run this command:

Note that using Pygments version 0.5.0 is highly recommended. Latest version of Pygmnents has issues with Jekyll.

```bash
gem install pygments.rb --version "=0.5.0"
```

## Running

9 - Start Jekyll
```bash
cd "proyect path"
jekyll serve
```

Jekyll proyect should be able to be created and browsed at localhost:4000.

## Troubleshooting

I make sure all the binaries of Ruby, Ruby Dev kit, Python are in path.

```bash
SET PATH=%PATH%;C:\ruby\bin;C:\devkit\bin;C:\git\bin;C:\Python;
```
Pygments not working

```bash
gem list
gem uninstall pygments.rb --version "=0.5.2"  ; or whatever version you got installed
gem install pygments.rb --version "=0.5.0"
```

## Contributing

We use the git-flow workflow, it's clean and helps us to keep order and trace code changes.

Check it here: [A successful Git branching model](http://nvie.com/posts/a-successful-git-branching-model/)

### Issuing

Make a [new issue](https://github.com/tecnoyucas/tecnoyucas.github.io/issues/new) at github.

Remember to push with a hashtag with the number of the issue, for example:

    git commit -am "Changed made #12345"

That will appear inside the 12345 issue.
