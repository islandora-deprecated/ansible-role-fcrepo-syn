# Ansible Role: Syn

An Ansible role that installs the Tomcat Valve [Syn](https://github.com/Islandora-CLAW/Syn) on:

* Centos/RHEL 7.x
* Ubuntu Xenial

## Role Variables

Available variables are listed below, along with default values:

Version of Syn to install:
```
fcrepo_syn_version: 0.1.0
```

Where to download Syn to:
```
fcrepo_syn_folder: /opt/syn
```

User to install Syn with:
```
fcrepo_syn_user: {{ tomcat8_server_user }}
```

Tomcat's home:
```
fcrepo_syn_tomcat_home: {{ tomcat8_home }}
```

Sites on Tomcat to install a key to decode JWTs:
```
fcrepo_syn_sites: []
# - url:
#   algorithm:
#   encoding:
#   anonymous:
#   default:
#   path:
#   key:
```

Static tokens to install in Syn:
```
fcrepo_syn_tokens: []
# - user:
# - roles:
# - token:
```

## Dependencies

* [islandora.tomcat8](https://github.com/Islandora-DevOps/ansible-role-tomcat8)
  
## Example Playbook

    - hosts: webservers
      roles:
        - { role: islandora.fcrepo-syn }

## License

MIT