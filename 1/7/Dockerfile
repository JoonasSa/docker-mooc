FROM ubuntu
RUN apt-get update && apt-get -y install curl
COPY curler.sh .
RUN chmod +x /curler.sh
CMD ["./curler.sh"]