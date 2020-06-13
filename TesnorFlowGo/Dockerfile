FROM ctava/tfcgo

RUN mkdir -p /model && \
    curl -o /model/iception5h.zip -s "https://download.tensorflow.org/models/iception5h.zip" && \
    unzip /model/iception5h.zip -d /model

WORKDIR /go/src/imgrecognition
COPY . .
RUN go build
ENTRYPOINT [ "/go/src/imgrecognition/imgrecognition" ]