FROM python

WORKDIR /app

# ADD requirements.txt requirements.txt
COPY requirements.txt requirements.txt

RUN pip install -r requirements.txt

EXPOSE 8888

ENTRYPOINT [ "jupyter", "lab" ]
CMD ["--ip='0.0.0.0'", "--port=8888", "--no-browser", "--allow-root"]
