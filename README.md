This is a simple flask server using connexion and swagger to generate an API endpoint.

## Installation

Clone this repository. create your virtual environment.

```
virtualenv --python=/usr/local/bin/python3.7 .env
```

Then install requirements:

```
pip install -r requirements.txt
```

then run the server:

```
python server.py
```

That's it !

You can see the endpoint locally:

```
http://localhost:5000/api/people
```

And the documentation here:

```
http://localhost:5000/api/ui/
```