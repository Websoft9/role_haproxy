Ansible Role: haproxy
=========

This Role is for installing [HAProxy Community](https://www.haproxy.org/) and configure its HAProxy Statistics Report, log file

## Requirements

Make sure these requirements need before the installation

| **Items**      | **Details** |
| ------------------| ------------------|
| Operating system | CentOS7.x Ubuntu18.04 AmazonLinux |
| Python verison | Python2  |
| Python components |    |
| Runtime |  |


## Related roles

This Role does not depend on other role variables in syntax, but it depend on other role before

```
roles:
    - {role: role_common, tags: "role_common"}
```


## Variables

The main variables of this Role and how to use them are as follows:

| **Items**      | **Details** | **Format**  | **Need to assignment** |
| ------------------| ------------------|-----|-----|
| haproxy_stats_username | "admin" | String | No |
| haproxy_stats_password | "123456"  | String | No |
| haproxy_stats_port | "1080" | String | No |

## Example

```
- name: Redis
  hosts: all
  become: yes
  become_method: sudo 
  vars_files:
    - vars/main.yml 

  roles:
    - { role: role_common }
    - { role: role_haproxy }
    ...
```

## FAQ
