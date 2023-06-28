FROM golang:1.20

RUN mkdir -p /home/webapp
WORKDIR /home/webapp
COPY . /home/webapp
RUN curl -sSfL https://raw.githubusercontent.com/cosmtrek/air/master/install.sh | sh -s -- -b $(go env GOPATH)/bin && \
    air -v
RUN go build -o app
CMD ./app
