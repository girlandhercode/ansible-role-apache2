Ansible Role for Apache2
========================

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
<td align="left">apache2_http_port</td>
<td align="left">yes</td>
<td align="left">80</td>
<td align="left"></td>
<td align="left">Apache2 HTTP listen port.</td>
</tr>
<tr class="even">
<td align="left">apache2_https_port</td>
<td align="left">yes</td>
<td align="left">443</td>
<td align="left"></td>
<td align="left">Apache2 HTTPS listen port.</td>
</tr>
<tr class="odd">
<td align="left">apahce2_timeout</td>
<td align="left">yes</td>
<td align="left">300</td>
<td align="left"></td>
<td align="left">Timeout: The number of seconds before receives and sends time out.</td>
</tr>
<tr class="even">
<td align="left">apache2_log_level</td>
<td align="left">yes</td>
<td align="left">warn</td>
<td align="left"></td>
<td align="left">LogLevel: Control the severity of messages logged to the error_log.</td>
</tr>
<tr class="odd">
<td align="left">apache2_module_name</td>
<td align="left">no</td>
<td align="left"><a href="https://github.com/pantarei/ansible-role-apache2/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td align="left"><ul>
<li><code>[]</code></li>
<li><code>list</code></li>
</ul></td>
<td align="left">Skip enable module if <code>[]</code>, or pass <code>list</code> as <code>name</code> to <a href="http://docs.ansible.com/ansible/apache2_module_module.html">apache2_module module</a>.</td>
</tr>
</tbody>
</table>

Dependencies
------------

-   [hswong3i.apt](https://github.com/pantarei/ansible-role-apt)
-   [hswong3i.ufw](https://github.com/pantarei/ansible-role-ufw)

Example Playbook
----------------

    - hosts: servers
      roles:
        - { role: hswong3i.apache2 }

License
-------

-   Code released under [MIT](https://github.com/pantarei/ansible-role-apache2/blob/master/LICENSE)
-   Docs released under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/)

Author Information
------------------

-   Wong Hoi Sing Edison
    -   <https://twitter.com/hswong3i>
    -   <https://github.com/hswong3i>

