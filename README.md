Apache2
=======

[![Build Status](https://travis-ci.org/pantarei/ansible-role-apache2.svg?branch=master)](https://travis-ci.org/pantarei/ansible-role-apache2)
[![GitHub tag](https://img.shields.io/github/tag/pantarei/ansible-role-apache2.svg)](https://github.com/pantarei/ansible-role-apache2)
[![GitHub license](https://img.shields.io/github/license/pantarei/ansible-role-apache2.svg)](https://github.com/pantarei/ansible-role-apache2/blob/master/LICENSE)
[![Ansible Role](https://img.shields.io/ansible/role/5972.svg)](https://galaxy.ansible.com/detail#/role/5972)

Ansible Role for Apache2 Installation.

Requirements
------------

This role require Ansible 1.9 or higher.

This role was designed for Ubuntu Server 14.04 LTS.

Role Variables
--------------

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">parameter</th>
<th align="left">required</th>
<th align="left">default</th>
<th align="left">choices</th>
<th align="left">comments</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left">apache2_module_name</td>
<td align="left">no</td>
<td align="left"><a href="https://github.com/pantarei/ansible-role-apache2/blob/master/defaults/main.yml">defaults/mail.yml</a></td>
<td align="left"><ul>
<li><code>null</code></li>
<li><code>list</code></li>
</ul></td>
<td align="left">Skip enable module if <code>null</code>, or pass <code>list</code> as <code>name</code> to <a href="http://docs.ansible.com/ansible/apache2_module_module.html">apache2_module module</a>.</td>
</tr>
</tbody>
</table>

Dependencies
------------

-   [hswong3i.apt](https://galaxy.ansible.com/detail#/role/5970)

Example Playbook
----------------

    - hosts: servers
      roles:
        - { role: hswong3i.apt, apt_cache_valid_time: 0, apt_upgrade: dist }
        - { role: hswong3i.apache2 }

License
-------

-   Code released under [MIT](https://github.com/hswong3i/ansible-role-apache2/blob/master/LICENSE)
-   Docs released under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/)

Author Information
------------------

-   Wong Hoi Sing Edison
    -   <https://twitter.com/hswong3i>
    -   <https://github.com/hswong3i>

