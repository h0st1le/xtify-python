About
=====

Python library for using the `Xtify
<http://xtify.com/>`_ web service API for mobile push notifications.

Requirements
============

Tested using Python 2.7, it will probably work on older versions. For versions
of Python 2.5 or earlier``simplejson`` will need to be installed.

Functionality
=============

As of version 0.1 only the Xtify Push API 2.0 is implemented. Mostly because it
was the only one I needed, at least for now...

Usage Examples
==============

    >>> import xtify
    >>> xtify = xtify.PushNotification(appKey='myAppKey', apiKey='myApiKey)
    >>> xtify.pushNotification.sendAll=True
    >>> xtify.pushNotification.content.subject='greetings earthling'
    >>> xtify.pushNotification.content.message='take me to your leader'
    >>> xtify.pushNotification.push()

    >>> import xtify
    >>> pushContent = xtify.PushContent(
        subject='greetings earthling', message='take me to your leader')
    >>> pushNotification = xtify.pushNotification(
        appKey='myAppKey', apiKey='myApiKey', sendall=True, content=pushContent)
    >>> pushNotification.push()

ChangeLog
=========

 * 0.1 Initial release
