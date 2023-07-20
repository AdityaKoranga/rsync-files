# rsync-files

#### For within the system/server:
```bash
mkdir new_directory && rsync -av --exclude=new_directory ./ ./new_directory/
```

>Note: Next time, this command will only copy the changed files

#### For sharing between two servers:

###### Use these cmd on destination server:
```bash
rsync -avz /local/directory/ username@remote_server:/remote/directory/
```
or
```bash
rsync -avz source_user@source_server:/path/to/source_directory/ .
```
For example: 
```bash
rsync -avz ubuntu@192.168.5.91:/home/ubuntu/new_directory .
```
- a: Archive mode, preserves permissions, ownership, and timestamps.
- v: Verbose output, shows details of the files being copied.
- z: Compresses data during transfer, reducing the network bandwidth required.
