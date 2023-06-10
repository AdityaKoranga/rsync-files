# rsync-files

For within the system/server:
```bash
mkdir new_directory && rsync -av --exclude=new_directory ./ ./new_directory/
```

`Next time, this command will only copy the changed files`

For sharing between two servers:
```bash
rsync -avz /local/directory/ username@remote_server:/remote/directory/
```
-avz are options passed to rsync. a stands for "archive", which tells rsync to copy directories recursively and to preserve symbolic links, file permissions, user & group ownerships, and timestamps. v stands for "verbose", which makes rsync show the progress of the copy operation. z stands for "compress", which tells rsync to compress the data as it's sent over the network, which can significantly speed up the transfer.
