## Emacs, make this -*- mode: sh; -*-

FROM rocker/r2u:noble

LABEL org.label-schema.license="GPL-2.0" \
      org.label-schema.vcs-url="https://github.com/rocker-org/" \
      org.label-schema.vendor="Rocker Project" \
      maintainer="Dirk Eddelbuettel <edd@debian.org>"

RUN apt update \
        && apt upgrade --yes \
        && apt install --yes --no-install-recommends \
                curl \
                devscripts \
                lsb-release \
                qpdf \
                sudo \
		wget \
	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds \
 	&& rm -rf /var/lib/apt/lists/* \
        && touch /etc/r2u_ci

