ARG BASE_IMAGE=alpine:3.15

FROM $BASE_IMAGE

ARG ARG_VAR=b
ENV ENV_VAR=${ARG_VAR}

RUN echo "ARG_VAR = ${ARG_VAR}, ENV_VAR = ${ENV_VAR}" > /tmp/test.txt
CMD ["/bin/sh", "-c", "cat /tmp/test.txt; echo ARG_VAR = ${ARG_VAR}, ENV_VAR = ${ENV_VAR}"]