{
  "info": {
    "name": "Google Adsense API Get Ad Units",
    "_postman_id": "dd8bda78-f02e-41e3-9c24-483b85d46ed9",
    "description": "List all ad units in the specified publisher's AdSense account.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Advertising",
      "item": [
        {
          "id": "b9f6e586-7ad5-456f-ae8b-fc203bce6b86",
          "name": "adsensehost.accounts.list",
          "request": {
            "url": "http://example.com/api/accounts?filterAdClientId=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "List hosted accounts associated with this AdSense account by ad client id."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "23ecab64-b0e3-40f9-8edd-60fc1f5fbd5c"
            }
          ]
        },
        {
          "id": "d9f82990-f73f-437f-8083-105cf6241eda",
          "name": "adsensehost.accounts.get",
          "request": {
            "url": {
              "protocol": "http",
              "host": "example.com",
              "path": [
                "api",
                "accounts/:accountId"
              ],
              "variable": [
                {
                  "id": "accountId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get information about the selected associated AdSense account."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "42a4dfde-cc2e-4284-88c6-40c3f17ff4dd"
            }
          ]
        },
        {
          "id": "70d91354-9ee3-423c-950f-296a22b281d6",
          "name": "adsensehost.accounts.adclients.list",
          "request": {
            "url": {
              "protocol": "http",
              "host": "example.com",
              "path": [
                "api",
                "accounts/:accountId/adclients"
              ],
              "query": [
                {
                  "key": "maxResults",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "pageToken",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "accountId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "List all hosted ad clients in the specified hosted account."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "dcdb7597-131f-4a4e-a6b1-418cf97f22bc"
            }
          ]
        },
        {
          "id": "bca9d5a7-b599-4518-bce7-b0de0515e0ef",
          "name": "adsensehost.accounts.adclients.get",
          "request": {
            "url": {
              "protocol": "http",
              "host": "example.com",
              "path": [
                "api",
                "accounts/:accountId/adclients/:adClientId"
              ],
              "variable": [
                {
                  "id": "accountId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "adClientId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get information about one of the ad clients in the specified publisher's AdSense account."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "155b8e82-56be-4224-9a41-b6a498305b01"
            }
          ]
        },
        {
          "id": "21acf00e-7837-4c87-8006-953f54e6e6eb",
          "name": "adsensehost.accounts.adunits.list",
          "request": {
            "url": {
              "protocol": "http",
              "host": "example.com",
              "path": [
                "api",
                "accounts/:accountId/adclients/:adClientId/adunits"
              ],
              "query": [
                {
                  "key": "includeInactive",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "maxResults",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "pageToken",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "accountId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "adClientId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "List all ad units in the specified publisher's AdSense account."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f7895f57-1a7f-4436-a69a-315a6eea06e7"
            }
          ]
        }
      ]
    }
  ]
}