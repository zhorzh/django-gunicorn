from python:3-slim

# install dependencies
copy ./requirements.txt /srv/requirements.txt
workdir /srv
run apt-get update
run apt-get install -y gcc
run apt-get install -y python-dev
run apt-get install -y libpq-dev
run pip3 install -r requirements.txt

# copy app code to container
copy /app /srv/app

# expose Flask port
expose 5000
