FROM alpine:3.7

RUN apk add --no-cache aria2

RUN mkdir -p /aria2/ /downloads/ &&\
    touch /aria2/sessions.txt &&\
    touch /aria2/logs.txt

ADD aria2.conf /aria2.conf
ADD move.sh /move.sh
RUN chmod +x /move.sh

EXPOSE 6890 6800

# CMD /bin/sh -c "echo $RPC_SECRET"
CMD /usr/bin/aria2c --enable-rpc --rpc-listen-all --continue=true --force-save=true --rpc-secret="$RPC_SECRET" --conf-path=/aria2.conf