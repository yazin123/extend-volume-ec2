# extend-volume-ec2

extend volume by going selecting storage and go to specific volume id and then extend the space

then
```bash
lsblk
```

You’ll see something like:

graphql
Copy
Edit
NAME          MAJ:MIN RM SIZE RO TYPE MOUNTPOINT
nvme0n1       259:0    0  16G  0 disk
├─nvme0n1p1   259:1    0  ...  ...



```bash
sudo growpart /dev/nvme0n1 1
```

```bash
sudo resize2fs /dev/nvme0n1p1
```

```bash
df -h
```