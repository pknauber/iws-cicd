# flask-example-cicd

This is a simple python flask application to host a simple web app.

After starting the flask application you can access following URL's on the server:

| Function        | URL                                     |
|-----------------|-----------------------------------------|
| index           | `http://<server>:<port>/`               |
| json            | `http://<server>:<port>/json/`          |
| hello           | `http://<server>:<port>/hello/`         |
| hello \<name>   | `http://<server>:<port>/hello/<name>`   |
| primes 100      | `http://<server>:<port>/primes/`        |
| primes \<count> | `http://<server>:<port>/primes/<count>` |


# Build and run

## Simple instructions (Debian/Ubuntu)

1. Install requirements:

```bash
apt update
apt install gcc musl-dev python3 python3-dev python3-pip
```
2. Build/Install project:

```bash
. build.sh
```

3. Run the server on **localhost:8080**:

```bash
. run.sh
```

## Advanced instructions

1. Install requirements:

    * python3
    * python3-dev
    * python3-pip
    * gcc (to compile cython)
    * musl-dev (to compile cython)

2. Build/Install project:

```bash
pip install -r requirements.txt
pip install -e .
```

3. Run the server on **localhost:8080**:

Set following environment variables:

```bash
export FLASK_APP=flaskr.app
export FLASK_ENV=stage
export FLASK_RUN_HOST=0.0.0.0
export FLASK_RUN_PORT=8080
```

for **Windows CMD** replace `export VARIABLE=VALUE` with `set VARIABLE=VALUE`

for **Windows Powershell** replace `export VARIABLE=VALUE` with `$env:VARIABLE = "VALUE"`

Then run the flask application with:

```bash
flask run
```