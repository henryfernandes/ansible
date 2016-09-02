# Start from a Debian image with the latest version of Go installed
# and a workspace (GOPATH) configured at /go.
FROM nginx

# Copy the local package files to the container's workspace.
#RUN mkdir -p /app && export GOPATH=/app && export PATH=$PATH:$GOPATH/bin && mkdir -p $GOPATH/src/github.com/user 
#RUN mkdir $GOPATH/src/github.com/user/goapp 
#RUN  mkdir -p /go/src/app
ADD default.conf /etc/nginx/conf.d/
CMD service nginx restart

# Build the outyet command inside the container.
# (You may fetch or manage dependencies here,
# either manually or with a tool like "godep".)
#RUN go install

# Run the outyet command by default when the container starts.
ENTRYPOINT service nginx restart && bash

# Document that the service listens on port 8080.
EXPOSE 80
