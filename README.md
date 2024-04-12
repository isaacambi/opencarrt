# OpenCart

# image of my opencart website
![](./images/opencart.png)



# opencart product list
![](./images/opencart2.png)

# opencart checkout page
![](./images/opencart3.png)


# mysql databse for customer details
![](./images/mysql4.png)



## Overview  
''' sudo apt update -y ''' #update the operating system

'''sudo apt install apache2'''  #Install Apache web Server

'''sudo systemctl start Apache2'''  #Start Apache2 service
'''sudo systemctl enable Apache2''' 
'''sudo systemctl status Apache2''' #verify status of service

'''sudo apt-get install php php-cli lipapache2-mod-php php-gd php-mysql php-zip php-curl '''  #php and additional modules to support opencart

'''php -v'''  #verify if php is installed
'''sudo mysql_secure_installation''' #secure installation

'''mysql -u root -p''' #log into your mysql shell

'''CREATE DATABASE opencart;'''
'''CREATE USER 'opencart'@'localhost'IDENTIFIED BY 'your-strong-password';
'''GRANT ALL PRIVILEGES ON opencart .* TO 'opencart' @'localhost';
'''FLUSH PRIVILEGES;'''
'''exit;'''

'''sudo wget https://github.com/opencart/opencart/releases/download/4.0.0.0/opencart-4.0.0.0.zip'''  #Download opencart

'''sudo apt -y install unzip'''  #unzip it 
''' sudo unzip opencart-4.0.0.0.zip -d /var/www/html/opencart/'''  #extract file into folder

'''sudo cp /var/www/html/opencart/upload/{config-dist.php,config.php}'''
'''sudo cp /var/www/html/opencart/upload/admin/{config-dist.php,config.php}'''

'''sudo chown -R www-data:www-data /var/www/html/opencart/''' #change ownership and enable permissions for the file
'''sudo chmod -R www-data:www-data /var/www/html/opencart/'''

'''sudo nano /etc/apache2/sites-available/opencart.conf''' #create virtualhost for opencart

'''sudo a2ensite opencart.conf'''  #to enable the site
'''sudo systemctl restart apache2'''  #restart apache2 to implement the changes

congratulations, you have successfully installed opencart!!


[![Minimum PHP Version](https://img.shields.io/badge/php-%3E%3D%207.4-8892BF.svg?style=flat-square)](https://php.net/)
[![GitHub release](https://img.shields.io/github/v/release/opencart/opencart)](https://github.com/opencart/opencart)
[![Lint](https://github.com/opencart/opencart/actions/workflows/Lint.yml/badge.svg)](https://github.com/opencart/opencart/actions/workflows/Lint.yml)

OpenCart is a free open source e-commerce platform for online merchants. OpenCart provides a professional and reliable foundation from which to build a successful online store.


## How to install

Please read the [installation instructions](INSTALL.md) included in the repository or download file.


## How to upgrade from previous versions

Please read the [upgrading instructions](UPGRADE.md) included in the repository or download file.

## Reporting a bug

Read the instructions below before you create a bug report.

 1. Search the [OpenCart forum](https://forum.opencart.com/viewforum.php?f=201), ask the community if they have seen the bug or know how to fix it.
 2. Check all open and closed issues on the [GitHub bug tracker](https://github.com/opencart/opencart/issues).
 3. If your bug is related to the OpenCart core code then please create a bug report on GitHub.
 4. READ the [changelog for the master branch](https://github.com/opencart/opencart/blob/master/CHANGELOG.md)
 5. Use [Google](https://www.google.com) to search for your issue.
 6. Make sure that your bug/issue is not related to your hosting environment.

If you are not sure about your issue, it is always best to ask the community on our [bug forum thread](https://forum.opencart.com/viewforum.php?f=201)

**Important!**
- If your bug report is not related to the core code (such as a 3rd party module or your server configuration) then the issue will be closed without a reason. You must contact the extension developer, use the forum or find a commercial partner to resolve a 3rd party code issue.
- If you would like to report a serious security bug please PM an OpenCart moderator/administrator on the forum. Please do not report concept/ideas/unproven security flaws - all security reports are taken seriously but you must include the EXACT details steps to reproduce it. Please DO NOT post security flaws in a public location.

## How to contribute

Fork the repository, edit and [submit a pull request](https://github.com/opencart/opencart/wiki/Creating-a-pull-request).

Please be very clear on your commit messages and pull request, empty pull request messages may be rejected without reason.

Your code standards should match the [OpenCart coding standards](https://github.com/opencart/opencart/wiki/Coding-standards). We use an automated code scanner to check for most basic mistakes - if the test fails your pull request will be rejected.

## Versioning

The version is broken down into 4 points e.g 1.2.3.4 We use MAJOR.MINOR.FEATURE.PATCH to describe the version numbers.

A MAJOR is very rare, it would only be considered if the source was effectively re-written or a clean break was desired for other reasons. This increment would likely break most 3rd party modules.

A MINOR is when there are significant changes that affect core structures. This increment would likely break some 3rd party modules.

A FEATURE version is when new extensions or features are added (such as a payment gateway, shipping module etc). Updating a feature version is at a low risk of breaking 3rd party modules.

A PATCH version is when a fix is added, it should be considered safe to update patch versions e.g 1.2.3.4 to 1.2.3.5

## Releases

OpenCart will announce to developers 1 week prior to public release of FEATURE versions, this is to allow for testing of their own modules for compatibility. For bigger releases (ones that contain many core changes, features and fixes) an extended period will be considered following an announced release candidate (RC). Patch versions (which are considered safe to update with) may have a significantly reduced developer release period.

The master branch will always contain an "_rc" postfix of the next intended version. The next "_rc" version may change at any time.

Developer release source code will not change once tagged.

If a bug is found in an announced developer release that is significant (such as a major feature is broken) then the release will be pulled. A patch version will be issued to replace it, depending on the severity of the patch an extended testing period may be announced. If the developer release version was never made public then the preceding patch version tag will be removed.

To receive developer notifications about release information, sign up to the newsletter on the [OpenCart website](https://www.opencart.com) - located in the footer. Then choose the developer news option.


## License

[GNU General Public License version 3 (GPLv3)](https://github.com/opencart/opencart/blob/master/LICENSE.md)

## Links

- [OpenCart homepage](https://www.opencart.com/)
- [OpenCart forums](https://forum.opencart.com/)
- [OpenCart blog](https://www.opencart.com/index.php?route=feature/blog)
- [How to documents](http://docs.opencart.com/en-gb/introduction/)
- [Newsletter](https://newsletter.opencart.com/h/r/B660EBBE4980C85C)
- [Discussions](https://github.com/opencart/opencart/discussions)
