FROM node:14.16.1

WORKDIR /src/app

COPY src/app/ .

RUN npm install && \
  # save node_modules マウント時node_moduleが消されてしまうので退避
  mv ./node_modules /

# node_module path パスを通す
ENV PATH $PATH:/node_modules/.bin
ENV HOST 0.0.0.0
EXPOSE 3000