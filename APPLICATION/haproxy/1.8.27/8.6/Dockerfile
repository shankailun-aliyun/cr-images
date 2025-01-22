FROM openanolis/anolisos:8.6

LABEL \
	org.opencontainers.image.title="haproxy" \
	org.opencontainers.image.version="1.8.27-8.6"

RUN yum -y update; \
	yum -y install haproxy; \
	yum clean all

ENV HAPROXY_VERSION 1.8.27

RUN set -eux; \
	chown haproxy:haproxy /var/lib/haproxy; \
	haproxy -v

STOPSIGNAL SIGUSR1

COPY docker-entrypoint.sh /usr/local/bin/

RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat

ENTRYPOINT ["docker-entrypoint.sh"]

CMD ["haproxy", "-f", "/etc/haproxy/haproxy.cfg"]
