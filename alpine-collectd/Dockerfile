FROM    alpine


RUN     apk update \
        && apk add collectd bash

# add a fake mtab for host disk stats
ADD     collectd.conf.tpl /etc/collectd/collectd.conf.tpl
COPY    docker-entrypoint.sh /docker-entrypoint.sh
RUN     chmod +x /docker-entrypoint.sh

ENTRYPOINT ["/docker-entrypoint.sh"]
CMD ["collectd", "-f"]
