### Free / Cheap Hosting
- https://www.linode.com/
- https://www.linode.com/linode-for-startups/
- https://www.digitalocean.com/
- https://hostingspell.com/
- https://cynderhost.com/
- https://www.ionos.com/
- https://www.hostm.com/lifetime-hosting
- https://squidix.com/shared-hosting/
- https://india.resellerclub.com/
- https://railway.app/
- https://thepowerhost.in/
- https://deno.com/deploy/pricing
- https://codesphere.com/pricing
- https://utho.com/

### PaaS for Hosting Custom apps
- https://www.porter.run/
- https://easypanel.io/
- https://www.cyclic.sh/
- https://railway.app/
- https://www.qovery.com/
- https://coolify.io/
- https://render.com/
- https://www.cloudron.io/

### Free / Cheap Storage
- https://www.backblaze.com/
- https://www.storj.io/pricing

**Clear Memory and Cache in Linux**
```
sync; echo 1 > /proc/sys/vm/drop_caches &&
sync; echo 2 > /proc/sys/vm/drop_caches &&
sync; echo 3 > /proc/sys/vm/drop_caches &&
swapoff -a && swapon -a &&
su -c "echo 3 >'/proc/sys/vm/drop_caches' && swapoff -a && swapon -a && printf '\n%s\n' 'Ram-cache and Swap Cleared'" root
```

```
sudo iptables -I INPUT 6 -m state --state NEW -p tcp --dport 80 -j ACCEPT
sudo netfilter-persistent save
```
https://docs.oracle.com/en-us/iaas/developer-tutorials/tutorials/apache-on-ubuntu/01oci-ubuntu-apache-summary.htm
