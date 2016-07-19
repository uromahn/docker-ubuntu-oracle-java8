FROM ubuntu:16.04
RUN apt-get -y update && apt-get install -y wget \
  software-properties-common \
  python-software-properties \
  git \
  build-essential \
  openssl \
&& add-apt-repository -y ppa:webupd8team/java \
&& apt-get -y update \
&& echo oracle-java8-installer shared/accepted-oracle-license-v1-1 select true | /usr/bin/debconf-set-selections \
&& apt-get install -y oracle-java8-installer \
&& apt-get install -y oracle-java8-set-default \
&& rm -rf /var/lib/apt/lists/* \
&& rm -rf /var/cache/oracle-jdk8-installer

# Define commonly used JAVA_HOME variable
ENV JAVA_HOME /usr/lib/jvm/java-8-oracle

# Define default command.
CMD ["bash"]
