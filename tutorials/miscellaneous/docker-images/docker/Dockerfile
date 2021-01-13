FROM busybox

ADD hello-world /bin/hello-world
# Secret echoed out for demonstration; don't do this with actually sensitive values
RUN --mount=type=secret,id=mycoolsecret,dst=/tmp/file_containing_secrets.txt cat /tmp/file_containing_secrets.txt
RUN cat /tmp/file_containing_secrets.txt

ENV NAME=world
ENTRYPOINT ["/bin/hello-world"]
