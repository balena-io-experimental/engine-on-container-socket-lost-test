FROM balenalib/raspberrypi3-ubuntu-node:17-bionic-20211208

# Install Docker, adapted from https://docs.docker.com/engine/install/ubuntu/
RUN apt-get update
RUN apt-get install -y ca-certificates curl gnupg lsb-release
RUN curl -fsSL https://download.docker.com/linux/ubuntu/gpg | gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
RUN echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | tee /etc/apt/sources.list.d/docker.list > /dev/null
RUN apt-get update
RUN apt-get install -y docker-ce-cli

CMD ["/usr/local/bin/node"]
