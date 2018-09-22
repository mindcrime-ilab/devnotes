
# How to remove packages installed today
The following command lists all packages installed today and save to a file:

```bash
grep -e `date +%Y-%m-%d` /var/log/dpkg.log | awk '/install / {print $4}' | uniq > todays_packages.lst
```
Afterwards the package list can be audited and feed into the ``apt`` command for removal:

```bash
cat todays_packages.lst | xargs sudo apt -y remove
```

> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTQyMzg2NDkzMl19
-->