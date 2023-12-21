# SimpleCart
implement simple cart and promotion

# Setup Guide


## Install, create and activate virtualenv
https://medium.com/analytics-vidhya/virtual-environment-6ad5d9b6af59

## Install requirements

    pip install -r requirements.txt
## create database
create new database, in this case we're using postgresql

## set env variable

create file .env in the root of the folder, and fill with you credential of your database

      
    DB_USER = ""
    DB_PASSWORD = ""
    DB_HOST = ""
    DB_PORT = ""
    DB_NAME = ""
    FLASK_DEBUG = true

## Create table

run `flask create`to create tables from models.

## Insert data product

run this query from your db client, in this case I'm using dbeaver
```
INSERT INTO public.product (sku, brand, "name", description, price, non_discountable) VALUES
    ('ABCD123', 'ABC Corporation', 'ABC Tea Bags', 'Premium tea bags', 15000.0, false),
    ('XYZ789', 'XYZ Foods', 'XYZ Instant Noodles', 'Delicious instant noodles', 5000.0, false),
    ('MNO456', 'MNO Drinks', 'MNO Sparkling Water', 'Refreshing sparkling water', 10000.0, true),
    ('PQR321', 'PQR Snacks', 'PQR Potato Chips', 'Crunchy potato chips', 8000.0, false);

```

## Run the app
to run the web app simply  use

    flask run

to access swagger use url `localhost:5000/apidocs`


## Run test
run test

    pytest

check test coverage

    pytest --cov=api test/

