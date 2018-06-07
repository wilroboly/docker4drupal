FROM haproxy:1.8

#ENV defaultRouteInterface = eth0
#ENV vpnSubnet = 10.0.0.0/32
#ENV dockerSubnet = 172.20.0.0/16
#ENV virtualIP = 10.100.13.140

RUN apt-get update \
	&& apt-get install -y --no-install-recommends \
	    iputils-ping \
	    curl \
        iptables \
        links \
	&& rm -rf /var/lib/apt/lists/*


#RUN iptables \
#    -j SNAT \
#    -t nat \
#    -I POSTROUTING 1 \
#    -o ${defaultRouteInterface} \
#    -d "${vpnSubnet}" \
#    -s "${dockerSubnet}" \
#    --to-source "${virtualIP}"

COPY haproxy.cfg /usr/local/etc/haproxy/haproxy.cfg