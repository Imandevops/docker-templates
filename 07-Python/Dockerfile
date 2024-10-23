FROM docker.arvancloud.ir/python:3.9-slim as build

WORKDIR /app

COPY . /app


RUN pip install --no-cache-dir -r requirements.txt

FROM docker.arvancloud.ir/python:3.9-alpine as final


WORKDIR /app


COPY --from=build /usr/local/lib/python3.9/site-packages /usr/local/lib/python3.9/site-packages
COPY --from=build /app /app


EXPOSE 5000


CMD ["python", "app.py"]
