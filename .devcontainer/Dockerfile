FROM mcr.microsoft.com/devcontainers/typescript-node:0-18-buster
# FROM node:18

RUN wget -q -O - https://packages.cloudfoundry.org/debian/cli.cloudfoundry.org.key | apt-key add - ; \
  echo "deb https://packages.cloudfoundry.org/debian stable main" | tee /etc/apt/sources.list.d/cloudfoundry-cli.list

RUN apt-get update \
  && apt-get -y install --no-install-recommends cf7-cli

RUN su node -c "npm i -g yo generator-easy-ui5"
# RUN npm i -g @ui5/cli

RUN su node -c "cf api https://api.cf.us10-001.hana.ondemand.com"