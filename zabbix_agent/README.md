Role Name
=========

A brief description of the role goes here.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------
# defaults file for zabbix_agent
zabbix_agent_logs_path: "/var/log/zabbix_agent"
zabbix_agent_logs_file: "{{ zabbix_agent_logs_path }}/zabbix_agent.log"

zabbix_agent_pid_path: "/var/run/zabbix"
zabbix_agent_pid_file: "{{ zabbix_agent_pid_path }}/zabbix_agent.pid"
zabbix_agent_ScriptsPath: "{{ zabbix_server_install_path }}/scripts"

zabbix_server_FpingLocation: "/usr/sbin/fping"
zabbix_server_conf_path: "{{ zabbix_server_install_path }}/etc"

zabbix_server_IncludeConfdir: "{{ zabbix_server_conf_path }}/zabbix_server.conf.d"
zabbix_agent_IncludeConfdir: "{{ zabbix_server_conf_path }}/zabbix_agentd.conf.d"

zabbix_server_ip: "192.168.201.220"



Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
