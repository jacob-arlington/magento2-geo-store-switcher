<h2>Welcome</h2>

ToBai Geo Store Switcher is a Magento 2 extension. It improves shopping experience on your Magento 2 Store. The module switches to the corresponding Website or Store View and your customers always get correct language locale, can use the currency which best suites them, get correct shipping rates and taxes. ToBai Geo Store Switcher extension uses MaxMind technology which accurately detects geo location of the customer by IP.

<h2>Installation</h2>

Please follow next instructions to successfully install ToBai Geo Store Switcher in your Magento 2 store.

1. Disable the cache with this command:

        bin/magento cache:disable

2. Add extension to composer require section using this command:

        composer require tobai/magento2-geo-store-switcher

3. Enable module and upgrade with this commands:

        bin/magento module:enable Tobai_GeoIp2
        bin/magento module:enable Tobai_GeoStoreSwitcher
        bin/magento setup:upgrade

4. Check under Stores->Configuration->Advanced->Advanced that the module ToBai_GeoStoreSwitcher is present. There also should be present ToBai_GeoIP2 extension which installs automatically. ToBai Geo Store Switcher is depended on ToBai GeoIP2 extension. If ToBai_GeoStoreSwitcher and ToBai_GeoIP2 display in alphabetical order, you successfully installed the reference module!

5. Flush and enable the cache with this commands:
        
        bin/magento cache:flush
        bin/magento cache:enable

Now you should see at Stores > Configuration new ToBai tab. When you click at this tab you will see Geo Store Switcher section.

<h2>Important</h2>

Since the Store Switcher extension depends on <a href="https://github.com/ytorbyk/magento2-geo-ip2">ToBai_GeoIP2</a> it should be configured previously.

and make sure you download country database from this URL
https://geolite.maxmind.com/download/geoip/database/GeoLite2-Country.tar.gz

extract GeoLite2-Country.mmdb and copy to

[Magento Root]/var/tobai-geoip/GeoLite2-Country.mmdb


<h2>Release notes:</h2>

<h3>v1.0.0</h3>

- First release.

<h3>v1.1.0</h3>

- Added support of store scope for enabling/disabling.

- Added support of website scope for all configuration.

- Added ability to disable module for specific IPs and/or user agents.

<h3>v1.1.1</h3>

- Bug: no redirect from non-base url.

<h3>v2.0.0</h3>

- Refactored the extension.
- Removed overwriting default store/store group/website.
