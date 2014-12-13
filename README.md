Role Name
=========

Install Zookeeper on Ubuntu Precice with Cloudera zookeepr-server package

Requirements
------------

Role Variables
--------------

Defaults: 

zookeeper_version: "3.4.5+cdh5.0.0+27-0.cdh5b2.p0.29.el6"
zookeeper_conf_dir: "/etc/zookeeper/conf"
zookeeper_data_dir: "/var/lib/zookeeper"

# Allow larger than default maximum client connections.
zookeeper_maxClientCnxns: 200

# The number of milliseconds of each tick
zookeeper_tickTime: 2000

# The number of ticks that the initial
# synchronization phase can take
zookeeper_initLimit: 100

# The number of ticks that can pass between
# sending a request and getting an acknowledgement
zookeeper_syncLimit: 5

# the port at which the clients will connect
zookeeper_clientPort: 2181

# the id which is used to initialize zookeeper server
zookeeper_id: 0

zookeeper_servers:
  - { zookeeper_id: "0", ip: "127.0.0.1", ports: "2888:3888" }


Dependencies
------------

Depends on smola.java


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD