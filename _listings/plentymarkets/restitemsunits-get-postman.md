{
  "info": {
    "name": "Plentymarkets List units",
    "_postman_id": "ace5199a-a1ef-49ef-9884-5c71901a676e",
    "description": "Lists all units.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "List",
      "item": [
        {
          "id": "1d1e6799-7506-4b39-befe-c2c3ed8c80f2",
          "name": "getRestItemsUnits",
          "request": {
            "url": "http://example.com/rest/items/units?updatedAt=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Lists all units."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "cd20521d-6b8f-4a64-90a8-d4171b904895"
            }
          ]
        }
      ]
    }
  ]
}