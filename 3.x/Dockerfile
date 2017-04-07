FROM colstrom/alpine

RUN apk-install openssl python3 gcc python3-dev build-base linux-headers \
    && wget https://bootstrap.pypa.io/get-pip.py -O - | python3 \
    && apk del openssl

ENTRYPOINT ["python3"]
