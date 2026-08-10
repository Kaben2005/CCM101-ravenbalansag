ravenbalansag@ubuntu:~$ cat /etc/os-release
PRETTY_NAME="Ubuntu 24.04.4 LTS"
NAME="Ubuntu"
VERSION_ID="24.04"
VERSION="24.04.4 LTS (Noble Numbat)"
VERSION_CODENAME=noble
ID=ubuntu
ID_LIKE=debian
HOME_URL="https://www.ubuntu.com/"
SUPPORT_URL="https://help.ubuntu.com/"
BUG_REPORT_URL="https://bugs.launchpad.net/ubuntu/"
PRIVACY_POLICY_URL="https://www.ubuntu.com/legal/terms-and-policies/privacy-policy"
UBUNTU_CODENAME=noble
LOGO=ubuntu-logo
ravenbalansag@ubuntu:~$ uname -r
6.8.0-136-generic
ravenbalansag@ubuntu:~$ lscpu | grep "Model name"
Model name:                              Intel Xeon E312xx (Sandy Bridge, IBRS update)
ravenbalansag@ubuntu:~$ df -h /
Filesystem      Size  Used Avail Use% Mounted on
/dev/vda1        19G  5.4G   13G  30% /
ravenbalansag@ubuntu:~$ nano system-information.md
