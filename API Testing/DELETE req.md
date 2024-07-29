# API Test: Delete order

## Request

- **URL**: `{{baseUrl}}/orders/:orderId`
- **Method**: DELETE

## Authorization

- **Type**: Token

## Path Variables

| Variable Name | Value                           |
|---------------|---------------------------------|
| `orderId`     | `Id of the order that was previously made` |

## Variables

| Variable Name | Value                       |
|---------------|-----------------------------|
| `baseUrl`     | `https://simple-books-api.glitch.me`   |

## Body

- **Empty**: This DELETE request does not require a request body.

## Tests

```javascript
pm.test("Status code is 204", function () {
    pm.response.to.have.status(204);
});
