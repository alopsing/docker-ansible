FROM python:2.7
MAINTAINER Sai Pola <sai.pola@pb.com>
RUN echo "===> Installing Ansible & Boto..."  && \
    pip --disable-pip-version-check --no-cache-dir install boto boto3 ansible==2.7.6 awscli && \
    pip install --upgrade pip && \
    pip install boto3 botocore awscli --upgrade && \
    \
    \
    echo "===> Adding handy tools..."  && \
    apt-get update && \
    apt-get install -y --no-install-recommends curl git zip jq unzip sshpass openssh-client groff && \
    mkdir -p /etc/ansible && \
    echo "localhost              ansible_connection=local ansible_python_interpreter=python" > /etc/ansible/hosts

# default command: display Ansible version
CMD [ "ansible-playbook", "--version" ]
