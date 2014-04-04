FROM bradrydzewski/java:openjdk6

WORKDIR /home/ubuntu
USER ubuntu
ADD rbenv.sh /etc/drone.d/

RUN export PATH=$PATH:/home/ubuntu/.rbenv/bin                                         && \
    cd ~/.rbenv/plugins/ruby-build                                                    && \
    git pull                                                                          && \
    export RBENV_VERSION=jruby-1.7.11                                                 && \
    eval "$(rbenv init -)"                                                            && \
    CC=gcc rbenv install jruby-1.7.11                                                 && \
    rbenv rehash                                                                      && \
    rbenv global jruby-1.7.11                                                         && \
    rbenv rehash                                                                      && \
    gem install bundler                                                               && \
    rbenv rehash