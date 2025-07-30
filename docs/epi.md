# EPI Survey SDS Schema

This document describes the schema for the EPI survey.

## Schema

Schema: [v1.json](/schemas/epi/v1.json)

**The table below only describes data that is survey specific. The generic structure of supplementary data is documented in [README.md](/docs/README.md)**

| Path                                | Description                                                                                                                                                                    | Mandatory |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| `identifier`                        | The unique top-level identifier. For business surveys this is the reporting unit reference without the check letter appended. RUREFS are changed to start with 0 and 1 for EPI | Yes       | 
| `supplier_number`                   | Like ruref, this is also a unique top-level identifier for the business. Same as RUREF. Supplier numbers are changed to start with 0 and 1 for EPI                             | Yes       |
| `current_month`                     | The current month and year that the data is required for.                                                                                                                      | Yes       |
| `items`                             | An object of items provided.                                                                                                                                                   | Yes       |
| `items.item[]`                      | The data about each item.                                                                                                                                                      | Yes       |
| `items.item[].identifier`           | The 10 digit unique reference for each item produced by the business. This number is allocated by ONS, if the item was to change the number would stay the same.               | Yes       |
| `items.item[].item_number`          | The 10 digit unique reference for each item produced by the business.                                                                                                          | Yes       |
| `items.item[].item_specification_1` | A separate field of the specification for the item produced by the business, the contents and order of this field can change dependent on the number of character.             | Yes       |
| `items.item[].item_specification_2` | A separate field of the specification for the item produced by the business, the contents and order of this field can change dependent on the number of character.             | No        |
| `items.item[].item_specification_3` | A separate field of the specification for the item produced by the business, the contents and order of this field can change dependent on the number of character.             | No        |
| `items.item[].item_specification_4` | A separate field of the specification for the item produced by the business, the contents and order of this field can change dependent on the number of character.             | No        |
| `items.item[].item_specification_5` | A separate field of the specification for the item produced by the business, the contents and order of this field can change dependent on the number of character.             | No        |
| `items.item[].unit_of_sale`         | The unit of sale for the item produced by the business.                                                                                                                        | Yes       |
| `items.item[].terms_of_sale_1`      | A separate field of the terms of sale for the item produced by the business, the contents and order of this field can change dependent on the number of characters.            | Yes       |
| `items.item[].terms_of_sale_2`      | A separate field of the terms of sale for the item produced by the business, the contents and order of this field can change dependent on the number of characters.            | No        |
| `items.item[].terms_of_sale_3`      | A separate field of the terms of sale for the item produced by the business, the contents and order of this field can change dependent on the number of characters.            | No        |
| `items.item[].terms_of_sale_4`      | A separate field of the terms of sale for the item produced by the business, the contents and order of this field can change dependent on the number of characters.            | No        |
| `items.item[].currency`             | The currency which the product price is recorded.                                                                                                                              | Yes       |
| `items.item[].country_of_origin`    | The country of origin for the item.                                                                                                                                            | Yes       |

## Examples

Examples can be found at [examples/epi](../examples/epi).