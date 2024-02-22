- [RHEL for Developers](https://developers.redhat.com/about)

- [RHEL in homelabs](https://www.redhat.com/sysadmin/linux-homelab-rhel)

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

## Reverse proxy & Web Server

- [RHEL Nginx](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/9/html-single/deploying_web_servers_and_reverse_proxies/index#setting-up-and-configuring-nginx_deploying-web-servers-and-reverse-proxies)

- [RHEL Certbox from pip](https://certbot.eff.org/instructions?ws=nginx&os=pip&tab=wildcard)

## Podman 

- [RHEL podman](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/9/html-single/building_running_and_managing_containers/index)

## Sources
- [User creation](https://linuxize.com/post/how-to-create-users-in-linux-using-the-useradd-command/)
