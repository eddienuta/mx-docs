---
id: es-index-epochinfo
title: epochinfo
---


## _id

The `_id` field of this index is represented by epoch.

## Fields

| Field            | Description                                                                                |
|------------------|--------------------------------------------------------------------------------------------|
| accumulatedFees  | The accumulatedFees field represents the accumulated fees that were payed in the epoch.    |
| developerFees    | The developerFees field represents the developer fees that were accumulated in the epoch.  |

## Query examples

### Fetch accumulatedFees and developerFees for a specific epoch

```
curl --request GET \
  --url ${ES_URL}/epochinfo/_search \
  --header 'Content-Type: application/json' \
  --data '{
	"query": {
		"match": {
			"_id":"600"
		}
	}
}'
```
