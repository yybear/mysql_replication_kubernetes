FROM docker.io/mysql

COPY my.cnf.tmpl /tmp/my.cnf.tmpl
# need random.sh because otherwise, ENV $RANDOM is not set
COPY random.sh /tmp/random.sh
RUN /tmp/random.sh

COPY docker-entrypoint.sh /entrypoint.sh
ENTRYPOINT ["/entrypoint.sh"]

EXPOSE 3306
CMD ["mysqld"]
