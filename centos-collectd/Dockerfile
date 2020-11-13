FROM    centos:7


RUN     yum install epel-release -y\
        && yum install collectd collectd-write_prometheus -y

ADD     collectd.conf.tpl /etc/collectd.conf.tpl
COPY    docker-entrypoint.sh /docker-entrypoint.sh
RUN     chmod +x /docker-entrypoint.sh

ENTRYPOINT ["/docker-entrypoint.sh"]
CMD ["collectd", "-f"]
