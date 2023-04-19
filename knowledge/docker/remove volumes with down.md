By default, `docker-compose down` does not remove [[volumes]] that are created by the services in the `docker-compose.yml` file. This is to prevent data loss in case you accidentally remove a volume that contains important data.

However, you can use the `--volumes` or `-v` flag with the [[Docker Compose]] down command to remove the volumes associated with the containers created by the `docker-compose up` command.

Here is an example:

```bash
docker-compose down -v
```

This command will stop and remove all [[containers]], networks, and volumes created by the `docker-compose up` command, including volumes that were created by services defined in the `docker-compose.yml` file.

Note that using this flag will permanently delete any data that was stored in the volumes, so use it with caution. If you want to keep the data in the volumes and reuse them in the future, you should not use this flag.