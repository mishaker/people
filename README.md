This is a simple microservice flask server using connexion and swagger to generate an API endpoint.

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

## What's happening?
The API documentation is in `swagger.yml`. This file can be edited manually or using swagger (OpenApi) editor.
`connexion` will create endpoints based on swagger file and flask will serve them.
Each endpoint and a method (ex. api/people and [GET]) will invoke a function.

In this case, from `swagger.yml`:

```
/people:
    get:
      operationId: "people.read"
```

We see that `/people` [GET] endpoint is bound to `read` function in `people.py`.
