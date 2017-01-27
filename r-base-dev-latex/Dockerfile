FROM mikebirdgeneau/r-base-dev-ext:latest
MAINTAINER Mike Birdgeneau <mike.birdgeneau@gmail.com>

RUN apt-get update

RUN apt-get install -y --no-install-recommends \
		texlive-latex-recommended \
		texlive-fonts-recommended \
		lmodern \
	&& apt-get clean \
	&& rm -rf /var/lib/apt/lists/*

CMD ["R"]
