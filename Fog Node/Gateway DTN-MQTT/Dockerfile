FROM python:2-alpine

WORKDIR /usr/src/app

COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt

COPY gateway-dtn-mqtt.py ./

COPY entrypoint.sh ./
RUN chmod +x entrypoint.sh

CMD [ "python", "gateway-dtn-mqtt.py" ]

ENTRYPOINT ["./entrypoint.sh"]