FROM bradrydzewski/base

WORKDIR /home/ubuntu
USER ubuntu

RUN sudo apt-get -qq update
RUN sudo apt-get --assume-yes install gcc-multilib xdg-utils libcurl4-openssl-dev

RUN wget -q http://downloads.dlang.org/releases/2013/dmd_2.064.2-0_amd64.deb && \
			sudo dpkg -i dmd_2.064.2-0_amd64.deb && \
			rm dmd_2.064.2-0_amd64.deb

RUN wget -q http://code.dlang.org/files/dub-0.9.20-linux-x86_64.tar.gz && \
            tar -xf dub-0.9.20-linux-x86_64.tar.gz && \
            rm dub-0.9.20-linux-x86_64.tar.gz && \
            sudo mv dub /usr/local/bin/dub
