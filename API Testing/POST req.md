# API Test: Submit an order on a book that isn't on stock

## Request

- **URL**: `{{baseUrl}}/orders`
- **Method**: POST

## Authorization

- **Type**: Token

## Variables

| Variable Name | Value                           |
|---------------|---------------------------------|
| `unavailableBookId`| Id of the book that was previously stored |
| `name`| Customers name |

## Body
```json
{
  "bookId": {{unavailableBookId}},
  "customerName": "{{name}}"
}
```

## Tests

```javascript
pm.test("Status code is 404", function () {
    pm.response.to.have.status(404);
});
