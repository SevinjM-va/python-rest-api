# Python REST API

Simple REST API for an online shop built with Flask.

## How to run the server

Open the project directory:

```bash
cd python-rest-api

Install the required dependencies:

pip install flask marshmallow

Start the server:
# Python REST API

Simple REST API for an online shop built with Flask.

## How to run the server

Open the project directory:

```bash
cd python-rest-api
```

Install the required dependencies:

```bash
pip install flask marshmallow
```

Start the server:

```bash
python main.py
```

The server will be available at:

```text
http://127.0.0.1:5000
```

## How to create a product

Send a POST request to:

```text
POST /api/v1/product
```

Example:

```bash
curl -X POST http://127.0.0.1:5000/api/v1/product -H "Content-Type: application/json" -d "{\"name\":\"Phone\",\"price\":500}"
```

Example response:

```json
{
  "id": "generated-product-id",
  "name": "Phone",
  "price": 500.0
}
```

## How to get all products

Send a GET request:

```text
GET /api/v1/product?page=0&limit=10
```

Example:

```bash
curl "http://127.0.0.1:5000/api/v1/product?page=0&limit=10"
```

The API returns a list of products.

## How to get a product by ID

Send a GET request:

```text
GET /api/v1/product/<id>
```

Example:

```bash
curl "http://127.0.0.1:5000/api/v1/product/fa4e0b91-2524-4ec5-a382-1336a8d8e933"
```

The API returns the product with the specified ID.
