# API Test: Create a Post with Random Data

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
