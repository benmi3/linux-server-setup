- [General setup](https://wiki.almalinux.org/documentation/installation-guide.html#installation)
- [After first boot](https://wiki.almalinux.org/documentation/after-installation-guide.html#update-the-system-and-check-for-security-updates)
- Create new user, add this user to wheel and docker group
```bash
sudo useradd -g users -G wheel,docker benmi3
```
- Check if it exists

```bash
sudo id benmi3
```

- Add passwd

```bash
sudo passwd benmi3
```

- Add Home Dir (If needed)

```bash
sudo useradd -m benmi3
```


## Sources
- [User creation](https://linuxize.com/post/how-to-create-users-in-linux-using-the-useradd-command/)
