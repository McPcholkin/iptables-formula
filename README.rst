===============
iptables-formula
===============

Simple formula to configure iptables (only basic functions).

.. note::
See the full `Salt Formulas installation and usage instructions <http://docs.saltstack.com/en/latest/topics/development/conventions/formulas.html>`_.

Available states
================

.. contents::
  :local:

``iptables``
------------
Installs iptables, iptables-persistent and add rules from pillar

``iptables.install``
--------------------
Installs iptables and iptables-persistent.

To remove rule from host set enabled to False:
::
  iptables:
    rules:
      ssh:
        enabled: False
        table: filter
        dport: 22
        jump: ACCEPT
        chain: INPUT
        protos: 
          - tcp


