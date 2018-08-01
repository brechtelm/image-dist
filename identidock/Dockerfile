FROM python:3.7
ENV http_proxy http://10.79.20.82:8080/
ENV https_proxy http://10.79.20.82:8080/
ENV HTTP_PROXY http://10.79.20.82:8080/
ENV HTTPS_PROXY http://10.79.20.82:8080/
RUN groupadd -r uwsgi && useradd -r -g uwsgi uwsgi
RUN pip install --upgrade pip
RUN pip install Flask==1.0.2 uWSGI==2.0.15 requests==2.19.1 redis==2.10.6
WORKDIR /app
COPY app /app
COPY cmd.sh /

EXPOSE 9090 9191
USER uwsgi

CMD ["/cmd.sh"]
