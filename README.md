- [RHEL](https://www.redhat.com/sysadmin/linux-homelab-rhel)
-[kubernetes setup](https://developer.ibm.com/tutorials/set-up-kubernetes-on-rhel-running-on-power/)

---
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

- [*If I go for nginx* Certbot](https://qiita.com/You_name_is_YU/items/661f2654fb6f21ff0eb9)

- [Traefik with podman](https://gerov.eu/posts/traefik-for-podman/🚡)


## Sources
- [User creation](https://linuxize.com/post/how-to-create-users-in-linux-using-the-useradd-command/)
