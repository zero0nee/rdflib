FROM docker.io/library/python:3.11.0-slim@sha256:1cd45c5dad845af18d71745c017325725dc979571c1bbe625b67e6051533716c

COPY docker/unstable/requirements.txt /var/tmp/build/

RUN \
    pip install -r /var/tmp/build/requirements.txt

COPY dist/*.whl /var/tmp/build/

RUN \
    pip install --no-deps /var/tmp/build/*.whl && \
    rdfpipe --version

ENTRYPOINT [ ]
