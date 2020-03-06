An Ansible role to install and manage mdadm raid arrays.

Role Variables example:
--------------

```yaml
mdadm_arrays:
  - number: 2
    # number of array ("/dev/md/" + item.number | string)
    devices:
      - '/dev/nvme0n1'
      - '/dev/nvme1n1'
    filesystem: 'ext4'
    # optional
    level: '1'
    mountpoint: '/data'
    # optional
    state: 'present'
    # present or absent
    opts: 'defaults,relatime,commit=20'
```

Be careful, no any checks, just creating and deleting arrays, any pull requests are welcome.