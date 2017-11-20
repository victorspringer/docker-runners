FROM cloud.canister.io:5000/victorspringer/docker-runner-base

RUN apt-get update \
  && apt-get install python-pip python-dev -y \
  && apt-get clean \
  && pip install --upgrade pip \
  && pip install --upgrade virtualenv \
  && pip install --upgrade awsebcli \
  && pip install --upgrade awscli \
  && mkdir ./temp && cd ./temp \
  && wget https://releases.hashicorp.com/terraform/0.9.11/terraform_0.9.11_linux_amd64.zip \
  && unzip terraform_0.9.11_linux_amd64.zip -d /usr/local/bin/ \
  && cd .. && rm -rf ./temp \
  && chmod +x /usr/local/bin/terraform

COPY aws /root/.aws

VOLUME ["/root/.aws"]

CMD ["/bin/bash"]