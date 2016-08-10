# Original source: https://raw.githubusercontent.com/prasmussen/glot-containers/master/clang/latest/Dockerfile

FROM rsmmr/clang:latest
MAINTAINER Madhav Jha "madhavjha@gmail.com"

# Add user
RUN groupadd fluent
RUN useradd -m -d /home/fluent -g fluent -s /bin/bash fluent

# Copy files
COPY $GOPATH/bin/fluent-runner /home/fluent/fluent-runner

USER fluent
WORKDIR /home/fluent/
CMD ["/home/fluent/fluent-runner"]
ENTRYPOINT "/home/fluent/fluent-runner"