# VCCW (vagrant-chef-centos-wordpress)

This is a Vagrant configuration designed for development of WordPress plugins, themes, or websites.

To get started, check out <http://vccw.cc/>

## Overview

* This Vagrant configuration has various settings you can change:
     * Multisite
     * Force SSL Admin
     * Subdirectory installation (e.g. http://wordpress.local/wp/)
* Customizable URL (default: http://wordpress.local/)
* Debug mode is enabled by default
* SSL is enabled by default
* Automatic installation & activation of plugins and themes at the time of provisioning:
     * default plugins: theme-check, plugin-check, dynamic-hostname
     * default theme: none
* Optional import of theme unit test data
* Pre-installed [wp-cli](http://wp-cli.org)
* Shares folders between Host and Guest OS

### Windowsでvagrant upするときの注意

* 明示的に `vagrant-hostsupdater` というプラグインをインストールしてやる必要がある。
* `C:/Windows/System32/drivers/etc`内部にあるhostsファイルに対して書き込みをするので、こいつにアクセス許可を与えてやる必要がある。

```:git bash
$ cd 
$ vagrant plugin install vagrant-hostsupdater
```
