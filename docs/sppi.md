# SPPI Survey SDS Schema

This document describes the schema for the SPPI survey.

## Schema

Schema: [v1.json](/schemas/sppi/v1.json)

**The table below only describes data that is survey specific. The generic structure of supplementary data is documented in [README.md](/docs/README.md)**

| Path                                       | Description                                                                                                                                                                                          | Mandatory |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| `identifier`                               | The unique top-level identifier. For business surveys this is the reporting unit reference without the check letter appended.                                                                        | Yes       |
| `source_quarter`                           | The quarter that business are asked to report for.                                                                                                                                                   | Yes       |
| `items`                                    | An object of items provided.                                                                                                                                                                         | Yes       |
| `items.service[]`                          | The data about each service.                                                                                                                                                                         | Yes       |
| `items.service[].identifier`               | The 10 digit unique reference for each service produced by the business. This number is allocated by ONS, if the service was to change the number would stay the same.                               | Yes       |
| `items.service[].item_number`              | The 10 digit unique reference for each service produced by the business. This number is allocated by ONS, if the service was to change the number would stay the same.                               | Yes       |
| `items.service[].service_description_1`    | Description of the service provided. Paper has a limit on the number of characters and therefore continuous text is split over multiple rows (service_description_1 through to 5).                   | Yes       |
| `items.service[].service_description_2`    | Description of the service provided. Paper has a limit on the number of characters and therefore continuous text is split over multiple rows (service_description_1 through to 5).                   | No        |
| `items.service[].service_description_3`    | Description of the service provided. Paper has a limit on the number of characters and therefore continuous text is split over multiple rows (service_description_1 through to 5).                   | No        |
| `items.service[].service_description_4`    | Description of the service provided. Paper has a limit on the number of characters and therefore continuous text is split over multiple rows (service_description_1 through to 5).                   | No        |
| `items.service[].service_description_5`    | Description of the service provided. Paper has a limit on the number of characters and therefore continuous text is split over multiple rows (service_description_1 through to 5).                   | No        |
| `items.service[].unit_of_sale`             | The unit of sale for the service delivered by the business.                                                                                                                                          | No        |
| `items.service[].terms_of_sale_1`          | The terms of sale for the service delivered by the business. Paper has a limit on the number of characters and therefore continuous text is split over multiple rows (terms_of_sale_1 through to 4). | No        |
| `items.service[].terms_of_sale_2`          | The terms of sale for the service delivered by the business. Paper has a limit on the number of characters and therefore continuous text is split over multiple rows (terms_of_sale_1 through to 4). | No        |
| `items.service[].terms_of_sale_3`          | The terms of sale for the service delivered by the business. Paper has a limit on the number of characters and therefore continuous text is split over multiple rows (terms_of_sale_1 through to 4). | No        |
| `items.service[].terms_of_sale_4`          | The terms of sale for the service delivered by the business. Paper has a limit on the number of characters and therefore continuous text is split over multiple rows (terms_of_sale_1 through to 4). | No        |
| `items.service[].currency`                 | The currency for the service delivered.                                                                                                                                                              | Yes       |
| `items.service[].currency_wording`         | The question wording associated with the currency for the service delivered.                                                                                                                         | Yes       |
| `items.service[].currency_wording_capital` | The question wording associated with the currency for the service delivered. With capital letter.                                                                                                    | Yes       |

## Examples

Examples can be found at [examples/sppi](../examples/sppi).