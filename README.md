cakephp-twitteroauth
====================

# Twitteroauth Plugin for CakePHP #

Version 1.0

The Twitteroauth plugin for CakePHP provides a (very) thin veil over abraham&#39;s twitteroauth for PHP for CakePHP 2.x applications.

## Usage ##

To use the Twitteroauth plugin for requests requiring authentication you must populate the following two lines in your `/app/Plugin/Twitteroauth/Controller/Component/TwitterComponent.php` file.

    'consumer_key' => 'your-twitter-consumer-key',
    'consumer_secret' => 'your-twitter-consumer_secret',
    'oauth_token' => 'your-twitter-oauth_token_secret',
    'oauth_token_secret' => 'your-twitter-oauth_token'

Don't forget to replace the placeholder text with your actual keys!

Keys can be obtained for free from the [developer Twitter website](https://dev.twitter.com).

Controllers that will be using twitteroauth require the Twitteroauth Component to be included.

In the controller simply call the twitteroauth method now available in the $this->Twitter->OAuth class.

    $result = Set::reverse($this->Twitter->OAuth->get(
       'legal/privacy', array()
    ));

To check the result simply use Set::reverse to convert the object into an array.

For twitteroauth documentation and methods, check https://github.com/abraham/twitteroauth/wiki/documentation

## Requirements ##

* PHP version: PHP 5.2+
* CakePHP version: Cakephp 2.0+