FROM ubuntu:18.04

RUN apt-get update && apt-get install -y \ 
    python3 \
    python3-pip  
RUN pip3 install jupyterlab

EXPOSE 8888

CMD ["jupyter", "lab", "--ip='0.0.0.0'", "--port=8888", "--no-browser", "--allow-root"]
