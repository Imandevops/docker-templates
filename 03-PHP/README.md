php

#set timezone tehran
RUN  rm -f /etc/localtime && ln -s /usr/share/zoneinfo/Asia/Tehran  /etc/localtime
