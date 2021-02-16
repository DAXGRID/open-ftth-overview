## Example GraphQL Query

```graphql
query {
  utilityNetwork {
    manufacturer {
      id
      name
      description
      deprecated
    }
  }
}
```

## Example result
```json
{
  "data": {
    "utilityNetwork": {
      "manufacturer": [
        {
          "id": "fd457db0-ad32-444c-9946-a9e5e8a14d17",
          "name": "Emtelle",
          "description": null,
          "deprecated": "False"
        },
        {
          "id": "47e87d16-a1f0-488a-8c3e-cb3a4f3e8926",
          "name": "GM Plast",
          "description": null,
          "deprecated": "False"
        }
      ]
    }
  }
}
```
