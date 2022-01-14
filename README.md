# VIP Skeleton

Welcome to VIP! This repo is a starting point for building your VIP site, including all the base folders to be built on.

## Guidebooks

We recommend starting with one of the following guidebooks:

* [Launching with VIP](https://docs.wpvip.com/how-tos/launch-a-site/)
* [VIP development workflow](https://docs.wpvip.com/technical-references/development-workflow/)
* [VIP local development](https://docs.wpvip.com/how-tos/local-development/)

## Usage

All the directories here are required and will be available on production web servers. Additional directories will not be available in production. For more information on how our codebase is structured, see https://docs.wpvip.com/technical-references/vip-codebase/.

## Directories

All the following directories are required and must not be removed:

* `client-mu-plugins`: for always active, global plugins (similar to `mu-plugins`) — see [our documentation](https://docs.wpvip.com/technical-references/vip-codebase/client-mu-plugins-directory/) for more information.
* `images`: Store your site's favicons here, per [this documentation](https://docs.wpvip.com/technical-references/vip-codebase/images-directory/). All other public-facing images should be uploaded or [imported](https://docs.wpvip.com/how-tos/launch-a-site-with-vip/launch-with-vip-migrate-content/) to the WordPress dashboard or stored as part of your `/theme/` assets.
* `languages`: For `.po` and `.mo` translation files, which specify the translated strings for the site — [more details here](https://docs.wpvip.com/how-tos/upload-languages-to-the-language-directory/).
* `plugins`: Your site's plugins — [more details here](https://docs.wpvip.com/technical-references/vip-codebase/plugins-directory/).
* `private`: Provides access to files that are not directly web accessible, but can be accessed by your theme or plugin code — [more details here](https://docs.wpvip.com/technical-references/vip-codebase/private-directory/).
* `themes`: Themes to be made available to your sites – [more details here](https://docs.wpvip.com/technical-references/vip-codebase/themes-on-vip-go/). We recommend keeping the default theme available for [testing purposes](https://docs.wpvip.com/how-tos/prepare-for-site-launch/testing-your-site/).
* `vip-config`: For custom configuration changes and additional `sunrise.php` [details](https://docs.wpvip.com/technical-references/multisites/sunrise-php/). This folder’s `vip-config.php` can be used to supply things usually found in `wp-config.php`. [More details here](https://docs.wpvip.com/technical-references/vip-codebase/vip-config-directory/).

These directories will also be available on production web servers. Any additional directories created in your GitHub repository that are not included in the above list will not be mounted onto your site, and so will not be web-accessible.

## PHPCS for checking coding standards

This repo contains a starting point for installing and using a _local_ version of [PHP_CodeSniffer](https://docs.wpvip.com/how-tos/php_codesniffer/) (PHPCS). To get started, you'll need to have [Composer](https://getcomposer.org/) installed, then open a command line at this directory, and run:

```sh
composer install
```

This will install PHPCS and register the below standards:

 - [VIP Coding Standards](https://github.com/Automattic/VIP-Coding-Standards)
 - [WordPress Coding Standards](https://github.com/WordPress/WordPress-Coding-Standards)
 - [PHPCompatibilityWP Standard](https://github.com/PHPCompatibility/PHPCompatibilityWP)

The [`.phpcs.xml.dist`](https://docs.wpvip.com/technical-references/vip-codebase/phpcs-xml-dist/) file contains a _suggested_ configuration, but you are free to amend this. You can also [extend](https://docs.wpvip.com/technical-references/vip-codebase/phpcs-xml-dist/#h-extending-the-root-phpcs-xml-dist-file-for-custom-themes-and-plugins) it for more granularity of configuration for theme and custom plugins.

To run PHPCS, navigate to the directory where the relevant `.phpcs.xml.dist` lives, and type:

```sh
vendor/bin/phpcs
```

See the [PHPCS documentation](https://github.com/squizlabs/PHP_CodeSniffer/wiki/Usage) (or run `phpcs -h`) for the available command line arguments.

## Support

If you need help with anything, VIP's support team is [just a ticket away](https://wpvip.com/accessing-vip-support/).

## Your content here

Feel free to add to or replace this README.md content with content unique to your project, for example:

* Project-specific notes; like a list of VIP environments and branches,
* Workflow documentation; so everyone working in this repo can follow a defined process, or
* Instructions for testing new features.
