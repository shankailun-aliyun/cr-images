FROM openanolis/anolisos:8.6

LABEL maintainer="OpenAnolis Cloud Native SIG"

RUN yum -y update; \
	yum -y install grafana; \
	yum clean all

ENV GF_PATHS_CONFIG="/etc/grafana/grafana.ini" \
	GF_PATHS_DATA="/var/lib/grafana" \
	GF_PATHS_HOME="/usr/share/grafana" \
	GF_PATHS_LOGS="/var/log/grafana" \
	GF_PATHS_PLUGINS="/var/lib/grafana/plugins" \
	GF_PATHS_PROVISIONING="/etc/grafana/provisioning"

WORKDIR $GF_PATHS_HOME

RUN chown -R "grafana:grafana" "$GF_PATHS_PROVISIONING"; \
	chmod -R 777 "$GF_PATHS_DATA" "$GF_PATHS_LOGS" "$GF_PATHS_PLUGINS" "$GF_PATHS_PROVISIONING"

EXPOSE 3000

COPY run.sh /run.sh

USER grafana

ENTRYPOINT ["/run.sh"]

