Role Name
=========

Role is designed to create master-master replication for PostgreSQL.

Example Playbook
----------------


- hosts: db_servers
  become: true
  roles:
     - {
       role: p3.postgresql-bdr,
       pgbdr_upstream_host: 10.0.1.210,
       pgbdr_database: sfm_db,
       pgbdr_monitoting: True,
       pgbdr_first_downstream_host: 10.0.1.220
     }

