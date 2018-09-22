
# How to remove packages installed today
The following command lists all packages installed today:

```bash
grep -e `date +%Y-%m-%d` /var/log/dpkg.log | awk '/install / {print $4}' | uniq
```

> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbMjExNjYxNzc1NV19
-->