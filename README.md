- [RHEL](https://www.redhat.com/sysadmin/linux-homelab-rhel)
- [kubernetes setup](https://developer.ibm.com/tutorials/set-up-kubernetes-on-rhel-running-on-power/)

---
- [General setup](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/9/html-single/performing_a_standard_rhel_9_installation/index)

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

- [Podman](https://technixleo.com/podman-buildah-on-rhel-centos-alma/#:~:text=Install%20Podman%20on%20RHEL%209%20%2F%20CentOS%209,the%20following%20command%20sudo%20yum%20install%20podman%20-y)

- [RHEL podman](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/9/html-single/building_running_and_managing_containers/index)

- [Traefik with podman](https://gerov.eu/posts/traefik-for-podman/🚡)

## Sources
- [User creation](https://linuxize.com/post/how-to-create-users-in-linux-using-the-useradd-command/)
