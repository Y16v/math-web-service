<h1 align="center"><b>Assignment</b></h3>

&nbsp;


## Installation

You run api service using docker containers or localhost

## Installing using docker

1. Run the command `docker-compose up -d` where the **docker-compose.yml** file located

## 📦 Backend Installation instructions

1. Install Python
2. Create viratualenv
```
python3 -m venv venv
```
3. Activate virtualenv
```
source venv/bin/activate
```

### ⚙️ Running dev server

Go to the `app` folder

In activated virtualenv install requirements:
```
pip install -r requirements.txt
```

Then run migrations:
```
./manage.py migrate
```

Run the backend dev server:
```
./manage.py runserver
```

### 🔨 Running tests

```
./manage.py test
```
&nbsp;


### Running Prometheus container

1. Uncomment `0.0.0.0:8000` target in a prometheus.yml file, which resides in promethues folder and comment `backend:8080` target

2. Run the prometheus container
```
docker run -d -p 9090:9090 --net=host -v ./prometheus/:/etc/prometheus prom/prometheus
```
&nbsp;

### Request sample

Now you can send request to the api server `localhost:8000/api/calculate/*algorithm*

To factorial 
```
{
    "number": 4
}
```

To fibonacci
```
{
    "number": 5
}
```

To ackermann 
```
{
    "number": 3,
    "number_2": 3
}
```