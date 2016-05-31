FROM ubuntu:latest
RUN apt-get update && apt-get install cron && apt-get clean
ADD crontab /etc/cron.d/hello-cron
RUN chmod 0644 /etc/cron.d/hello-cron
RUN touch /var/log/cron.log
CMD /usr/sbin/cron && tail -f /var/log/cron.log
