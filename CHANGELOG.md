Changelog
=========

1.4.1
-----

* Allow PHP 8.0

1.4
---

* PHP requirement bumped to 7.2, tested with up to 7.4.

1.3
---

* performance #145 improve XML parsing
* bugfix #142 Add referrer in requests to jackrabbit to avoid CSRF errors on jackrabbit 2.12.4 and newer
* feature #130 Added function to client to set global curl-options. With the factory, you can use
  the parameter `jackalope.jackrabbit_curl_options` to set curl options as hashmap.
* feature #128 Version label support

1.2
---

* Fixed Property::getNode() can return the same node multiple times if that
  node was added to the property multiple times. This has the side effect that
  the array returned by this method is not indexed by uuid anymore. That index
  was never advertised but might have been used.
* RepositoryFactoryJackrabbit::getRepository now throws a PHPCR\ConfigurationException
  instead of silently returning null on invalid parameters or missing required
  parameters.

1.1.0
-----

* Performance improvements: The fetchDepth feature is now fully supported.
* Support for logging PHPCR database queries.
* mix:lastModified fields can be handled automatically.
* Commands cleanup, check cli-config.php.dist.

1.1.0-RC1
---------

* **2014-01-04**: mix:lastModified is now handled automatically. To disable,
  set the option jackalope.auto_lastmodified to `false`.

* **2013-12-26**: cleanup of phpcr-utils lead to adjust cli-config.php.dist.
  If you use the console, you need to sync your cli-config.php file with the
  dist file.

* **2013-12-14**: Added support for logging PHPCR database queries.
