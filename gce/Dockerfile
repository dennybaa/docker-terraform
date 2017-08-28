FROM google/cloud-sdk
USER 1000:1000
ENV TF_VERSION 0.10.2

# Install terraform
RUN apt-get install unzip && curl -sSL https://releases.hashicorp.com/terraform/${TF_VERSION}/terraform_${TF_VERSION}_linux_amd64.zip -o /tmp/terraform.zip && \
        cd /usr/bin && unzip /tmp/terraform.zip && rm -rf /tmp/*

# Create unprivileged user
RUN useradd -mU user -u 1000

VOLUME ["/home/user", "/data"]
WORKDIR /data
