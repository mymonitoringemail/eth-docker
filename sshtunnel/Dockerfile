FROM alpine:latest

RUN apk add openssh-client

ENV REMOTE_HOST_ADDRESS localhost
ENV REMOTE_HOST_PORT 5052
ENV LOCAL_PORT 5052
ENV SSH_PORT 22
ENV SSH_USER user

CMD /usr/bin/ssh -o UserKnownHostsFile=/var/hosts/known_hosts -L 0.0.0.0:$LOCAL_PORT:localhost:$REMOTE_HOST_PORT -N -i /var/keys/remote_key -p $SSH_PORT $SSH_USER@$REMOTE_HOST_ADDRESS

