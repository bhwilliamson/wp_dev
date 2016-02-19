FROM php:5.6-cli

RUN apt-get update -y && apt-get install -y git

WORKDIR /usr/src
RUN mkdir wcms2

RUN git clone https://github.com/squizlabs/PHP_CodeSniffer.git phpcs
RUN git clone -b master https://github.com/WordPress-Coding-Standards/WordPress-Coding-Standards.git wpcs

ENV PATH /usr/src/phpcs/scripts:$PATH

RUN cd phpcs && ./scripts/phpcs --config-set installed_paths ../wpcs && \
./scripts/phpcs --config-set default_standard WordPress

WORKDIR /usr/src/wcms2
RUN mkdir src
WORKDIR /usr/src/wcms2/src

CMD ["/bin/bash"]

