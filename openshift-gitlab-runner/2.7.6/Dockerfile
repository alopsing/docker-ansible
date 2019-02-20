FROM alopsing/ansible:2.7.6
RUN pip install --upgrade pip
RUN pip install boto3 botocore awscli --upgrade
RUN chmod g=u /etc/passwd
COPY run.sh run.sh
ENTRYPOINT [ "run.sh" ]
USER 1001
