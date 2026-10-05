# Linux

| Command  | Description      |
| :------- | :--------------- |
| Ctrl + D | hide all windows |

| Command     | Description                          |
| :---------- | :----------------------------------- |
| passwd      | change system password               |
| hostnamectl | system summary, including OS version |

Backgrounds located in `/usr/share/backgrounds`

Fix error [Error mounting /dev/sdc1 at /media/rob/ Elements: wrong fs type, bad option, bad superblock on dev/sdc1, missing codepage or helper program, or other error.](https://askubuntu.com/questions/1520035/wrong-fs-type-bad-option-bad-superblock-on-dev-sdc1-missing-codepage-or-helpe):

```
sudo ntfsfix -b -d /dev/sdc1
```
