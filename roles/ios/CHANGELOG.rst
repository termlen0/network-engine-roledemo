===============================
ios
===============================

devel
=====

Major Changes
-------------

- complete refactoring of `load_config` to support merge and replace better



v1.0.1
======

Minor Changes
-------------

- the ``load_config`` function will now return the full config diff

v1.0.0
======

Major Changes
-------------

- Initial release of the ``ios`` role.

- This role provides a set of functions for working with Cisco IOS/IOS-XE based
  devices for performing operational and configuration tasks


New Functions
-------------

- NEW ``get_facts`` Returns a set of facts from the Cisco IOS device

- NEW ``get_config`` Returns the device running or startup configuration

- NEW ``load_config`` Merge or replace the current device configuration

