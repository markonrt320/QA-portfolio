# API Test: Update order

## Request

- **URL**: `{{baseUrl}}/orders/:orderId`
- **Method**: PATCH

## Authorization

- **Type**: Token

## Path Variables

| Variable Name | Value                           |
|---------------|---------------------------------|
| `orderId`     | `Id of the order that was previously made` |


## Variables

| Variable Name | Value                           |
|---------------|---------------------------------|
| `baseUrl`| `https://simple-books-api.glitch.me` |
| `randomFullName`| `Random full name` |

## Body

```json
{
  "customerName": "{{$randomFullName}}"
}
```

## Tests

```javascript
pm.test("Body matches string", function () {
    pm.response.to.have.status(204);
    
});
