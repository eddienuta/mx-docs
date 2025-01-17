---
id: es-index-validators
title: validators
---


## _id

The `_id` field of this index is composed in this way: `{shardID}_{epoch}` (example: `1_123`)

## Fields

| Field       | Description                                                                                     |
|-------------|-------------------------------------------------------------------------------------------------|
| publicKeys  | The publicKeys field contains a list of all validators' public keys from an epoch and a shard.  |


## Query examples

#### Fetch all validators from a shard by epoch
In the example below, we fetch all the validators' public keys from shard 1, epoch 600.

```
curl --request GET \
  --url ${ES_URL}/validators/_search \
  --header 'Content-Type: application/json' \
  --data '{
	"query": {
		"match": {
			"_id":"1_600"
		}
	}
}'
```