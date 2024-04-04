# galera cluster for docker-compose

To evaluate galera cluster with docker compose, this is a basic template to spawn multiple containers acting as a test cluster on a single host.


# Adding a new node

- copy node3 definition in docker-compose.yml and increment to `node4`
- edit **all** files in galera-config: Append `,node4` into `wsrep_cluster_address` line
- `cp galera-config/node3.conf galera-config/node4.conf` and change the `wsrep_node_name` to `node4`
