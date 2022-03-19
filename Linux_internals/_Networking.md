[JVNS networking zine](https://jvns.ca/networking-zine.pdf).

[Task-centered iproute2 user guide](https://baturin.org/docs/iproute2/)

> iproute2 is the Linux networking toolkit that replaced net-tools (ifconfig, vconfig, route, arp etc.). The ip command comes from the iproute2 package, as well as tc and a few others.

> Note that iproute2 is not new, it has been a standard Linux tool since the early 2000's. It's been included in every distro by default, or at least available from the repos for a very long time.

> If you are not sure if something is a correct host address, use ipcalc or similar program to check.

[traffic shaping with tc](https://serverfault.com/questions/70042/linux-traffic-shaping-using-tc). [more](https://www.badunetworks.com/traffic-shaping-with-tc/). [more](https://netbeez.net/blog/how-to-use-the-linux-traffic-control/). [more](https://wiki.debian.org/TrafficControl). [more](https://wiki.archlinux.org/index.php/Advanced_traffic_control).

> TC bundled with iproute2 package in Debian.

[How To Use IPRoute2 Tools to Manage Network Configuration on a Linux VPS](https://www.digitalocean.com/community/tutorials/how-to-use-iproute2-tools-to-manage-network-configuration-on-a-linux-vps)

[Anatomy of a Linux DNS Lookup – Part I](https://zwischenzugs.com/2018/06/08/anatomy-of-a-linux-dns-lookup-part-i/). [Part II](https://zwischenzugs.com/2018/06/18/anatomy-of-a-linux-dns-lookup-part-ii/). [Part III](https://zwischenzugs.com/2018/07/06/anatomy-of-a-linux-dns-lookup-part-iii/). [Part IV](https://zwischenzugs.com/2018/08/06/anatomy-of-a-linux-dns-lookup-part-iv/). [Part V](https://zwischenzugs.com/2018/09/13/anatomy-of-a-linux-dns-lookup-part-v-two-debug-nightmares/).

> that’s exactly the reason why I always use getent hosts example.org when shell scripting. it uses the c call, queries the system’s host database and honors nsswitch. 

[DNS lookups in Kubernetes](https://www.reddit.com/r/programming/comments/ey6mf0/dns_lookups_in_kubernetes/)

[A journey to searching Have I Been Pwned database in 49μs](https://news.ycombinator.com/item?id=22459661)

[	Must, Should, Don't Care: TCP Conformance in the Wild](https://news.ycombinator.com/item?id=22785086)

[cows](https://twitter.com/uhoelzle/status/1263333281891708929)

[observability stuff](https://twitter.com/copyconstruct/status/1270071495897702400)

[Migrating Dropbox from Nginx to Envoy](https://news.ycombinator.com/item?id=24000546)

[Logging tracing and metrics](https://techbeacon.com/enterprise-it/monitoring-demystified-guide-logging-tracing-metrics). [bg talk](https://www.youtube.com/watch?time_continue=966&v=GsMs3n8CB6g&feature=emb_logo).

[The Illustrated TLS Connection](https://tls.ulfheim.net/) [hn](https://news.ycombinator.com/item?id=24167873)

[How to take back control of /etc/resolv.conf on Linux](https://news.ycombinator.com/item?id=24390053)

[NAT Slipstreaming](https://news.ycombinator.com/item?id=24955891)

[Wifi collisions](https://witestlab.poly.edu/blog/channel-planning-in-802-11-understanding-the-effect-of-nearby-networks/)

[How to get better wireless signal](https://www.howtogeek.com/126327/how-to-get-a-better-wireless-signal-and-reduce-wireless-network-interference/)

[visual guide to SSH tunnels](https://news.ycombinator.com/item?id=26053323)

    One thing to add is that you can even open tunnels during an interactive session without disconnection.

    To do this, type the escape command sequence ~C (will not show) and it will drop you to the control prompt. You can then add tunnels.

     ssh>
     ssh> -L 8000:localhost:9000 
     Forwarding port.
     
[change your mac address](https://news.ycombinator.com/item?id=26060152)

[A brief history of router architecture](https://news.ycombinator.com/item?id=26442845)

[Routing the technical interview](https://lars.hupel.info/articles/routing-the-interview/)

[Protocol detection and opaque ports in Linkerd](https://www.cncf.io/blog/2021/03/10/protocol-detection-and-opaque-ports-in-linkerd/)

[Liberating Kubernetes From Kube-proxy and Iptables](https://www.youtube.com/watch?v=bIRwSIwNHC0). [iptables](https://www.youtube.com/watch?v=NAdJojxENEU)

[Slack's Migrating Millions of Websockets from HAProxy to Envoy](https://www.youtube.com/watch?v=douKdQRgDEQ).

[The Sisyphean Task of DNS Client Config on Linux](https://news.ycombinator.com/item?id=26821298)

[ the case of the 50ms request](https://twitter.com/b0rk/status/1390012478386577411)

[	Netcat – All you need to know ](https://news.ycombinator.com/item?id=27973020)

[Writing a toy traceroute from scratch](https://news.ycombinator.com/item?id=30140380)

[ephemeral ports](https://news.ycombinator.com/item?id=30181710)

[What does it mean to listen on a port?](https://news.ycombinator.com/item?id=30323865)

[Basic Network Troubleshooting](https://news.ycombinator.com/item?id=30317540)

[Simuladores para virtualizar redes y aprender routing y switching](https://www.redeszone.net/tutoriales/redes-cable/programas-simular-red/)

[   How NAT traversal works (2020) ](https://news.ycombinator.com/item?id=30707711)


