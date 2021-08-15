FROM ubuntu:focal-20201106

ENV TZ=US/Eastern
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

# install appropriate programs
RUN apt-get update && \
	apt-get install -y \
	curl \
	apt-utils \
	git \
	python3 \
	build-essential \
	python3-pip \
	android-tools-adb \
	aapt \
	apksigner \
	wget \
	zipalign \
	unzip

RUN pip3 install frida
RUN pip3 install frida-tools
RUN pip3 install objection

RUN wget https://raw.githubusercontent.com/iBotPeaches/Apktool/master/scripts/linux/apktool -O /bin/apktool
RUN wget https://bitbucket.org/iBotPeaches/apktool/downloads/apktool_2.5.0.jar -O /bin/apktool.jar
RUN wget https://github.com/skylot/jadx/releases/download/v1.2.0/jadx-1.2.0.zip -O /tmp/jadx-1.2.0.zip && \
	unzip -a /tmp/jadx-1.2.0.zip

RUN chmod +x /bin/apktool
