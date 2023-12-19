# SSG - Secure Shell GUI (elgentos fork)

## Background
This program shows a pretty GUI for all the SSH server connections found in your SSH config file. It also allows you to connect to them.
Simply type to filter and use the arrow keys to select. Press enter to open the SSH connection.

*You must have an existing SSH Configuration file for this application to be useful. See examples [here](http://www.cyberciti.biz/faq/create-ssh-config-file-on-linux-unix/)*

*By default, this application will look for your config file in ``~/.ssh/config``*

![image](https://github.com/elgentos/ssg-js/assets/431360/eccbeb9c-b26f-4a4d-93f2-32bb8c62f0b8)

## Installation
1. Install using `npm install -g ssg-js`
2. Run ``ssg`` or alternatively ``ssg /path/to/ssh/config/file``
3. Enjoy all your visualised server connections.

## How to use
Run ``ssg`` from the command line. All server connections in your config file will appear. You can filter them by typing. Filtering works on Description, Tags and server names.

Select the desired server you want to connect to by using the arrow keys. When selected, press the ENTER key. Alternatively, press ESC if you wish to exit.

## Adding descriptions
As SSH config doesn't come with an ability to add a description or tags, you must put in lines similar to the following in order to get the description and tag fields populated.

```
	# @description My awesome description
	Host uniquehostname
		Hostname awesomehost.local
		User ubuntu
```

All ``@description`` must be declared _before_ your host definition.

# Changelog

### Version 0.4.0 (2023-12-19)
* Removed GCP support
* Added [Hypernode Brancher](https://www.hypernode.com/en/brancher/) support

### Version 0.3.0 (2021-11-19)
* Removed DigitalOcean support
* Removed AWS support
* Changed GCP support from listing Kubernetes clusters to Compute Instances

### Version 0.2.0 (2019-02-14)
* Added DigitalOcean droplet listing when `doctl` is available
* Added caching of DigitalOcean results in cache file
* Added CTRL+R refresh option for cache file

### Version 0.1.5 (2016-07-17)
* ssg will now show AWS servers if you happen to have the `aws` CLI configured
* Minor bugfixes

### Version 0.1.4 (2016-01-21)
* NodeJS Minimum engine version added (Issue #4)
* Now hosts separated by spaces will be displayed on dedicated lines (Issue #3)

### Version 0.1.3 (2016-01-06)
* Updated documentation. Screenshots etc.

### Version 0.1.2 (2016-01-04)
* JS Docs
* Updated Readme (ssg-js rather than ssg)
* Colours
* Ability to specify custom config file

### Version 0.1.1
* Minor Bugfixes

### Version 0.1.0 (2015-15-21)
* Initial release
