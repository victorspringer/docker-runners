FROM cloud.canister.io:5000/victorspringer/docker-runner-base

RUN curl -sL https://deb.nodesource.com/setup_8.x | bash -
RUN apt-get update && apt-get install -y --no-install-recommends \
	nodejs \
	&& rm -rf /var/lib/apt/lists/*

RUN npm install -g serve
