# Login-with-Facebook-using-PHP
Nowadays users are not interested in filling a big form to registration. Short registration process helps to get more subscribers for your website. Login with Facebook is a quick and powerful way to integrate registration and login system on the website. Facebook is a most popular social network and most of the users have a Facebook account. Facebook Login allow users to sign into your website using their Facebook account credentials without sign up on your website. 


# Database Table Creation

To store the user information from the Facebook database, a table (users) need to be created in MySQL database. At first, create a database (like codexworld) and run the below SQL on the database. The following SQL creates a users table with some basic fields in the database to hold the Facebook profile information.

```sh

CREATE TABLE `users` (
 `id` int(11) NOT NULL AUTO_INCREMENT,
 `oauth_provider` enum('','facebook','google','twitter') COLLATE utf8_unicode_ci NOT NULL,
 `oauth_uid` varchar(100) COLLATE utf8_unicode_ci NOT NULL,
 `first_name` varchar(50) COLLATE utf8_unicode_ci NOT NULL,
 `last_name` varchar(50) COLLATE utf8_unicode_ci NOT NULL,
 `email` varchar(100) COLLATE utf8_unicode_ci NOT NULL,
 `gender` varchar(10) COLLATE utf8_unicode_ci NOT NULL,
 `locale` varchar(10) COLLATE utf8_unicode_ci NOT NULL,
 `picture` varchar(255) COLLATE utf8_unicode_ci NOT NULL,
 `link` varchar(255) COLLATE utf8_unicode_ci NOT NULL,
 `created` datetime NOT NULL,
 `modified` datetime NOT NULL,
 PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_unicode_ci;

```