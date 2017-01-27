FROM mikebirdgeneau/r-base-dev-ext:latest
MAINTAINER Mike Birdgeneau <mike.birdgeneau@gmail.com>

RUN apt-get update -qq \
	&& apt-get upgrade -y

RUN apt-get install -y --no-install-recommends \
		texlive-latex-recommended \
	&& apt-get clean \
	&& rm -rf /var/lib/apt/lists/*

CMD ["R"]
