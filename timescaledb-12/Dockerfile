# vim: set noexpandtab ts=4 sw=4 nolist:

FROM timescale/timescaledb:latest-pg12-oss

RUN apk add --no-cache python3 py3-pip
RUN pip install awscli

COPY docker-entrypoint.sh /usr/local/bin/
COPY backup.sh /usr/local/bin/
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]

CMD ["run-cron"]
