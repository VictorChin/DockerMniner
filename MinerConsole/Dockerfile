FROM ubuntu:18.04

RUN apt-get update \
&& apt-get -qq --no-install-recommends install \
ca-certificates \
&& apt-get install unzip \
&& rm -r /var/lib/apt/lists/*

RUN wget -q --content-disposition https://minergate.com/download/xfast-ubuntu-cli \
&& unzip MinerGatexFast-cli-1.2-amd64.zip

ENTRYPOINT ["minergate-cli/minergate-cli"]
CMD ["-u", "junk@objectmage.com", "--zec"]