Ansible Role: haproxy
=========

This Role is for installing [HAProxy Community](https://www.haproxy.org/) and configure its ，并配置stats，开启日志

## Requirements

Make sure these requirements need before the installation

| **Items**      | **Details** |
| ------------------| ------------------|
| Operating system | CentOS7.x Ubuntu18.04 AmazonLinux |
| Python 版本 | Python2  |
| Python 组件 |    |
| Runtime |  |


## Related roles

This Role does not depend on other role variables in syntax, but it depend on other role before

```
roles:
    - {role: role_common, tags: "role_common"}
    - {role: role_redis, tags: "role_redis"}
```


## Variables

The main variables of this Role and how to use them are as follows:

| **Items**      | **Details** | **Format**  | **Need to assignment** |
| ------------------| ------------------|-----|-----|
| redis_version | [ 2.8,3.0,3.2,4.0,5.0,stable ] | 字符串 | 否 |
| redis_install | True,False | 布尔 | 否 |
| redis_install_redisinsight | False, True| 布尔 | 否 |

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
    - { role: role_redis }
    ...
```

## FAQ
