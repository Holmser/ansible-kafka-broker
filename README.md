[andrewrothstein.kafka-broker](https://galaxy.ansible.com/andrewrothstein/zookeeper/)
=========

Install a [Kafka](https://kafka.apache.org/) broker.
Assumes an accessible ZooKeeper quorum. Consider [ZooKeeper cluster](https://github.com/andrewrothstein/ansible-zookeeper-cluster)

Requirements
------------

See [meta/main.yml](meta/main.yml). Assumes a running ZooKeeper cluster.

Role Variables
--------------

See [defaults/main.yml](defaults/main.yml)

Dependencies
------------

See [meta/main.yml](meta/main.yml)

Example Playbook
----------------

inventory.ini
```ini
[zookeeper-quorum]
zk-host[1:3]

[kafka-broker]
kb-host1 kafka_broker_id=1
kb-host2 kafka_broker_id=2
kb-host3 kafka_broker_id=3
...
```

```yml
- hosts: kafka-broker
  roles:
    - andrewrothstein.kafka-broker
```

License
-------

MIT

Author Information
------------------

Andrew Rothstein <andrew.rothstein@gmail.com>
