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

[a primer on proxies](https://news.ycombinator.com/item?id=30736610)

[Online IP Address Class Finder](https://ipaddress.standingtech.com/online-ip-address-class-finder-detector)

["Connections", in computer networking, are completely fake and make-believe](https://twitter.com/crdudeyoutube/status/1530330152550293505)

[how do videogames stay in sync?](https://news.ycombinator.com/item?id=31512257)

[what they don't teach you about sockets](https://news.ycombinator.com/item?id=32225532)

[Getting started with nmap](https://ittavern.com/getting-started-with-nmap/)

[LINEAR CONSTRAINTS: THE PROBLEM WITH O(1) FREEZE](https://www.tweag.io/blog/2023-01-26-linear-constraints-freeze/)

[AWS Route 53 CNAME - dot at end of target value or not?](https://serverfault.com/questions/861134/aws-route-53-cname-dot-at-end-of-target-value-or-not#_=_). [Trailing Dots in Domain Names](http://www.dns-sd.org/trailingdotsindomainnames.html)

[Using multiple A-records for my domain](https://webmasters.stackexchange.com/questions/10927/using-multiple-a-records-for-my-domain-do-web-browsers-ever-try-more-than-one)

[CNAME vs A DNS Records](https://webmasters.stackexchange.com/questions/6882/what-are-cname-and-a-dns-records)

> A cname record is a pointer that points to a fully qualified domain name(fqdn), an A Record is a pointer that points to an ip adress.

[Learning DNS in 10 Years](https://twitter.com/b0rk/status/1654478221813882880)

[See this page fetch itself, byte by byte, over TLS](https://news.ycombinator.com/item?id=35884437)

[k8s networking tweet](https://twitter.com/davidfowl/status/1657533910551756800)

[The Difference Between Root Certificate Authorities, Intermediates, and Resellers](https://www.agwa.name/blog/post/roots_intermediates_and_resellers)

[mitmproxy: Support 'http_proxy' and 'https_proxy' variables](https://github.com/mitmproxy/mitmproxy/issues/3296). Beware! This is for mitmproxy itslef. But you're usually interested in setting these variables for you server.

[Are HTTP_PROXY, HTTPS_PROXY and NO_PROXY environment variables standard?](https://superuser.com/questions/944958/are-http-proxy-https-proxy-and-no-proxy-environment-variables-standard)

[intercepting http proxy - disadvantages compared to a normal proxy](https://stackoverflow.com/questions/9274836/intercepting-http-proxy-disadvantages-compared-to-a-normal-proxy). [Intercept a macOS app traffic using mitmproxy](https://www.codejam.info/2021/07/intercept-macos-app-traffic-mitmproxy.html).

[why is DNS still hard to learn?](https://news.ycombinator.com/item?id=36909427)

[rollback network code](https://twitter.com/SebAaltonen/status/1687691543157829632)

[Unix sockets, Cygwin, SSH agents, and sadness](https://news.ycombinator.com/item?id=37304370)

[Running one’s own root Certificate Authority in 2023](https://news.ycombinator.com/item?id=37537689)

[Can I use Tailscale alongside other VPNs?](https://tailscale.com/kb/1105/other-vpns/)

[Whats the difference between a port forwarder and a socks proxy?](https://serverfault.com/questions/92447/whats-the-difference-between-a-port-forwarder-and-a-socks-proxy). [Transparent SOCKS proxy in Go to replace NAT (2016)](https://www.reddit.com/r/golang/comments/4abaie/transparent_socks_proxy_in_go_to_replace_nat/)

> The simplest answer is that port-forwarding (as in NAT) is generally transparent to the client, while a SOCKS (or HTTP) proxy requires the client to explicitly use the proxy protocol.

> I agree with the above definitions, though I'd add that NAT and Proxies have a very different purpose. NAT is simply routing: there is no caching, and there is no real "oversight" for lack of a better word. Proxies are put in place for caching, monitoring, traffic shaping. They are very much about control.

> A NAT device performs "address translation" (tuple [TCP/UDP port:IP address] to another tuple) whereas a proxy terminates (in networking terms) a protocol layer, performs adaptation (again in networking terms) and rebuilds another a connection towards the destination.

> In other words, a NAT tries to be as "transparent" to the client protocol as can be whereas a PROXY is really "two connections back-to-back" (same or different protocols on each side).

> SOCKS is a simple proxy protocol mostly for tunneling TCP connections. With SOCKS5, clients can ask SOCKS server to create tunnels with a IPv4/IPv6 address or a DNS domain name. For this, SOCKS is not as transparent as NAT.

[Virtual networking 101: Bridging the gap to understanding TAP](https://blog.cloudflare.com/virtual-networking-101-understanding-tap/) 

[Use of HTTPS Resource Records](https://www.netmeister.org/blog/https-rrs.html)

[WireGuard vs. Tailscale · Tailscale](https://tailscale.com/compare/wireguard)

[Investigation of a Cross-regional Network Performance Issue](https://netflixtechblog.medium.com/investigation-of-a-cross-regional-network-performance-issue-422d6218fdf1)

[#vibr and #vnet](https://hachyderm.io/@brokenix@emacs.ch/112813219092015649)

[The New Internet](https://tailscale.com/blog/new-internet)

[   How I learned to stop worrying and love userspace networking ](https://news.ycombinator.com/item?id=41390412)

[Optimizing global message transit latency: a journey through TCP configuration](https://news.ycombinator.com/item?id=41291470)

[the journey of an internet packet](https://news.ycombinator.com/item?id=41327394)

[Noisy neighbor detection with eBPF](https://news.ycombinator.com/item?id=41513860)

[How Raw sockets behave differently in macOS and Linux ](https://news.ycombinator.com/item?id=41537426)

[A terrible way to jump into colocating your own stuff](https://rachelbythebay.com/w/2024/09/22/colo/). [hn](https://news.ycombinator.com/item?id=41622653).

[reducing WebSocket traffic by 40%:](https://discord.com/blog/how-discord-reduced-websocket-traffic-by-40-percent)

[Connect to colleagues' local servers from anywhere](https://tailscale.com/kb/1034/local-team-server). [video](https://www.youtube.com/watch?v=YzBJSiBezCs). [Easily Access Your Self-Hosted Apps Remotely Using Tailscale](https://www.youtube.com/watch?v=d8FyQKAVJtQ). [Remotely access and share your self-hosted services](https://www.youtube.com/watch?v=Vt4PDUXB_fg). [Self Hosting with Tailscale and Caddy](https://dev.to/dracarys18/self-hosting-with-tailscale-and-caddy-4o94). [own domains?](https://www.reddit.com/r/Tailscale/comments/1fbl03x/is_it_possible_to_use_my_own_domains_for/). [Is HTTPs necessary?](https://www.reddit.com/r/Tailscale/comments/18dy2qa/is_https_necessary/). [enabling HTTPs](https://tailscale.com/kb/1153/enabling-https). [Tailscale on Android](https://tailscale.com/kb/1079/install-android). [Why Tailscale?](https://tailscale.com/why-tailscale). [Make Service accessible externally through tailscale?](https://www.reddit.com/r/Tailscale/comments/14b4qym/make_service_accessible_externally_through/). [Tailscale Funnel](https://tailscale.com/kb/1223/funnel). [Tailscale to the rescue](https://www.ajfriesen.com/tailscale-to-the-rescue/). [Tailscale HTTPs](https://www.reddit.com/r/Tailscale/comments/18dy2qa/comment/kcoojm0/). [Using HTTPS in your homelab](https://grumpy.systems/2023/using-https-in-your-homelab-and-why-its-important/). [machine names](https://tailscale.com/kb/1098/machine-names). [Solutions](https://tailscale.com/kb/1355/solutions).

[Confused about the definition of self hosting](https://www.reddit.com/r/selfhosted/comments/191er2j/confused_about_the_definition_of_self_hosting/). [why self-host](https://news.ycombinator.com/item?id=41440855).

[CGNAT and self-hosting](https://www.reddit.com/r/selfhosted/comments/170ku6z/has_anyone_been_able_to_successfully_self_host/). [video](https://www.youtube.com/watch?v=aAzdn9cqYRY). [video](https://www.youtube.com/watch?v=7TOwr1Hs9fk). [DDOSing](https://bsky.app/profile/tef.bsky.social/post/3lgfvodmdrs2u)

[How netcat can listen to the same port on the same host from two different terminals?](https://stackoverflow.com/questions/37570647/how-netcat-can-listen-to-the-same-port-on-the-same-host-from-two-different-termi). [two apps on the same port](https://stackoverflow.com/questions/1694144/can-two-applications-listen-to-the-same-port)

[Unshare and port forwarding into namespace](https://serverfault.com/questions/1151515/unshare-and-port-forwarding-into-namespace). [Is it possible to run 'unshare -n [program]' as an unprivileged user?](https://unix.stackexchange.com/questions/252714/is-it-possible-to-run-unshare-n-program-as-an-unprivileged-user). [Network namespace & slirp4netns - access namespaced network from host](https://unix.stackexchange.com/questions/637159/network-namespace-slirp4netns-access-namespaced-network-from-host). [Network namespaces to the Internet with veth and NAT](https://josephmuia.ca/2018-05-16-net-namespaces-veth-nat/)











