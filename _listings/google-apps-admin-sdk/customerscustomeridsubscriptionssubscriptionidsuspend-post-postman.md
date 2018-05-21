{
  "info": {
    "name": "Google Apps Admin SDK API Suspect Subscription",
    "_postman_id": "5f5fcf34-24c5-4180-ab5c-02d8447cd448",
    "description": "Suspends an active subscription.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "LicenseSubscription",
      "item": [
        {
          "id": "3d7c9483-ef4b-49d6-951f-ebbccfcba807",
          "name": "reseller.subscriptions.suspend",
          "request": {
            "url": {
              "protocol": "http",
              "host": "example.com",
              "path": [
                "api",
                "customers/:customerId/subscriptions/:subscriptionId/suspend"
              ],
              "variable": [
                {
                  "id": "customerId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "subscriptionId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Suspends an active subscription."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "febb5854-85cc-4f4a-b100-fc621756388d"
            }
          ]
        }
      ]
    }
  ]
}