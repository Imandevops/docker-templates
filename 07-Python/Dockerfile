FROM python:3.10-slim-buster

WORKDIR /app

COPY requirements.txt requirements.txt
RUN pip3 install -r requirements.txt
#set timezone tehran
#set timezone tehran
RUN  rm -f /etc/localtime && ln -s /usr/share/zoneinfo/Asia/Tehran  /etc/localtime


COPY . .

CMD [ "python3", "-m" , "flask", "run" ]
