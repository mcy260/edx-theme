# starter-theme-openedx

![Starter theme screenshot](screenshot.png)

Starter theme for developing comprehensive theme on Open edX

## How to use

1. Change to `edxapp` user

		$ sudo -u edxapp bash


3. Move to that folder

		$ cd /edx/app/edxapp/themes

4. Clone this repo

		$ git clone https://github.com/mcy260/edx-theme.git my-theme

5. Make some changes in `l/edx/app/edxapp/lms.env.json' Then change some variables to this:

		ENABLE_COMPREHENSIVE_THEMING: true,
		COMPREHENSIVE_THEME_DIRS: ["/edx/app/edxapp/themes"],
		DEFAULT_SITE_THEME: "my-theme",

6. Back to ubuntu sudo users, and restart the edxapp to load new configuration.

		$ exit
		$ sudo /edx/bin/supervisorctl restart edxapp:

7. Run the `update.sh` script. To apply the themes.

		$ cd /edx/app/edxapp/edx-platform/themes/my-theme/
		$ sh update.sh



