.. include:: /Includes.rst.txt

.. _breaking-101305-1689059968:

==================================================================================
Breaking: #101305 - Introduce type declarations for some methods in GeneralUtility
==================================================================================

See :issue:`101305`, :issue:`101453`

Description
===========

Native return and param type declarations have been introduced for the following
methods of :php:`\TYPO3\CMS\Core\Utility\GeneralUtility`:

- :php:`array2xml`
- :php:`cmpFQDN`
- :php:`cmpIP`
- :php:`cmpIPv4`
- :php:`cmpIPv6`
- :php:`explodeUrl2Array`
- :php:`getUrl`
- :php:`get_tag_attributes`
- :php:`implodeArrayForUrl`
- :php:`implodeAttributes`
- :php:`intExplode`
- :php:`isOnCurrentHost`
- :php:`isValidUrl`
- :php:`locationHeaderUrl`
- :php:`normalizeIPv6`
- :php:`revExplode`
- :php:`sanitizeLocalUrl`
- :php:`split_tag_attributes`
- :php:`trimExplode`
- :php:`validEmail`
- :php:`validIP`
- :php:`validIPv4`
- :php:`validIPv6`
- :php:`validPathStr`
- :php:`wrapJS`
- :php:`xml2arrayProcess`
- :php:`xml2array`
- :php:`xml2tree`
- :php:`xmlRecompileFromStructValArray`

Impact
======

Calling any of the mentioned methods with invalid types will result in a
PHP error.

Affected installations
======================

Only those installations that use the mentioned methods with invalid types.

Migration
=========

Make sure to pass parameters of the required types to the mentioned methods.

.. index:: PHP-API, NotScanned, ext:core
