# JAMVI
JAMVI is the company that seeks to bridge the gap of farmers financing by providing farmers with last mile technology so as they can have the access of  digital wallets, alternative credit portfolio and micro-lending platform specifically for the farmers.


### Getting started
#### Using Docker
> This assumes you have [docker](https://www.docker.com/) and [docker-compose](https://docs.docker.com/compose/) installed.

* Clone the repo
* `cd JAMVI`
* run `docker-compose up`. The initial build will take some time because it's pulling the image for the first time. Consecutive builds will be faster.
* The `docker-compose.yml` exposes the port `5003:80`. That means that the application in on port `5003`. To test using `curl` on a terminal run:

`$ curl http://localhost:5003/api/at_gateway`

#### Using virtualenv
> Ensure that you have [python 3](https://www.python.org/download/releases/3.0/) installed

* Clone the repo
* `cd JAMVI`
* run `virtualenv -p python3 .venv`
* run `pip install -r requirements.txt`
* run `python manage.py migrate --noinput`
* run `python manage.py collectstatic --noinput`
* run `python manage.py runserver`