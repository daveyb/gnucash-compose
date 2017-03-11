# gnucash-compose
docker-compose file(s) to bring up local gnucash cluster

# use
1. Set `$GNUCASH_DATA_PATH` and `$MYSQL_ROOT_PASSWORD` environment variables.
- `$GNUCASH_DATA_PATH` is the local path where the gnucash data will be stored.
- docker-compose expects the following directories: `homedir`, `config`.
- additional directories may be required depending on the data drive chosen, e.g. `mysql.

2. Run `docker-compose up` from within the desired data driver directory to configure and start the cluster.

3. X11 is forwarded to the host OS. Set xhost to allow connections from localhost with `xhost +LOCAL:`
