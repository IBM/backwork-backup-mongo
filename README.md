# monsoon-backup-mongo
Add support for MongoDB backups on [`monsoon`](https://github.ibm.com/apset/monsoon).

## Requirements
This plug-in is build on top of [`mongodump`](https://docs.mongodb.com/manual/reference/program/mongodump/#bin.mongodump),
so you will need to have [`mongo-tools`](https://github.com/mongodb/mongo-tools)
installed. 

If you already have the `mongod` server or `mongo` client installed then you 
should have `mongodump`. If not, you can install them using the 
[official packages](https://docs.mongodb.com/manual/tutorial/install-mongodb-on-ubuntu/#packages)
or build from [source](https://github.com/mongodb/mongo-tools).

## Installing
You can use `pip` to install this plug-in directly from GHE:
```sh
pip install git+ssh://git@github.ibm.com/apset/monsoon-backup-mongo
```

## Using
After installing the plug-in you will be able to use the `backup mongo` command
on `monsoon`.

```sh
monsoon backup mongo
```

You can pass any option that you would normally use on `mongodump`:

```sh
monsoon backup mongo --user=user --password=pass --host=mongo
```

The only exception is `-h` which is reserved for the help/usage message, so the
host needs to be passed as `--host`.
