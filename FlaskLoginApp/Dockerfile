# init a base image (Alpine is small Linux dist)
FROM alpine:latest

RUN apk add py3-pip
RUN apk add --no-cache python3-dev \
    && pip install --upgrade pip

# define the present working directory
WORKDIR /flaskloginapp
# copy the contents into the working dir
COPY . /flaskloginapp
# run pip to install the dependencies of the flask app
RUN pip --no-cache-dir install -r requirements.txt
# provide port 5000
EXPOSE 5000
# define the command to start the container
ENTRYPOINT ["python3"]
CMD ["manage.py"]