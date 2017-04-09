FROM colstrom/alpine

RUN apk-install openssl python3 gcc python3-dev build-base linux-headers git bash \
    && wget https://bootstrap.pypa.io/get-pip.py -O - | python3 \
    && apk del openssl \
    && pip3 install discord.py pluginbase psutil gitpython pyparsing pyspeedtest requests tqdm \
    && git clone https://github.com/1byte2bytes/Starbot.git /Starbot
    && echo cd /Starbot > run.sh
    && echo python3 main.py >> run.sh
    && chmod +x run.sh

ENTRYPOINT ["./run.sh"]
