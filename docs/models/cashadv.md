# Cash Advance

## Overview

The Cash Advance model is designed to evaluate the creditworthiness of an individual or business based on their financial history and credit score. It is used to determine the likelihood of a loan being repaid on time.

## How to Use

### Example Request

```bash
curl -X POST "https://your-api-url/v1/score" \
-H "x-api-key: your_api_key" \
-H "x-client-id: your_client_id" \
-F "file=@path_to_your_file.json" \
-F "model=cashadvance"
```

### Example Response

```json
{
  "model": {
    "adverse_action_items": [
      {
        "AA_Description": "Average amount of salary advance payments in last 1 month",
        "AA_code": "AA4"
      },
      {
        "AA_Description": "Number of days the daily overall balance in cash/checking/saving accounts was less than $1000 in last 1 month",
        "AA_code": "AA17"
      },
      {
        "AA_Description": "Number of salary advance payments made below $100 in last 6 months",
        "AA_code": "AA34"
      },
      {
        "AA_Description": "Number of ecommerce payments made over $5 in last 1 month",
        "AA_code": "AA25"
      }
    ],
    "model_name": "cashadvance",
    "pred_prob": 0.1163879930973053,
    "score": 696.0
  }
}
```
