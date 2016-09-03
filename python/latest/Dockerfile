# Original source: https://github.com/prasmussen/glot-containers/blob/master/python/latest/Dockerfile

FROM python:latest
MAINTAINER Madhav Jha "madhavjha@gmail.com"

# Add user
RUN groupadd fluent
RUN useradd -m -d /home/fluent -g fluent -s /bin/bash fluent

# Install libs
RUN pip install \
    cachetools \
    nose \
    numpy \
    python-dateutil \
    pytz \
    six

# Copy files
COPY bin/linux_386/fluent /home/fluent/fluent

USER fluent
WORKDIR /home/fluent/
CMD ["-stream=false"]
ENTRYPOINT ["/home/fluent/fluent"]