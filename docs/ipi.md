# Prodcom Survey SDS Schema

This document describes the schema for the ipi survey.

## Schema

Schema v1: [v1.json](/schemas/ipi/v1.json)

**The table below only describes data that is survey specific. The generic structure of supplementary data is documented in [README.md](/docs/README.md)**

| Path                                         | Description                                                              | Mandatory                       |
|----------------------------------------------|--------------------------------------------------------------------------|---------------------------------|
| `items.items[].identifier`                   | The 10 digit unique reference for each item produced by the business. This number is allocated by ONS, if the item was to change the number would stay the same.                                                                                    | Yes                             |
| `items.items[].item_number`                  | The 10 digit unique reference for each item produced by the business. This number is allocated by ONS, if the item was to change the number would stay the same.                                                                                    | Yes                             |
| `items.items[].item_specification_1`         | A separate field of the specification for the item produced by the business, the contents and order of this field can change dependent on the number of characters. This line is always PRODUCT.                                                       | Yes                             |
| `items.items[].item_specification_2`         | A separate field of the specification for the item produced by the business, the contents and order of this field can change dependent on the number of characters.                                                                                    | No                              |
| `items.items[].item_specification_3`         | A separate field of the specification for the item produced by the business, the contents and order of this field can change dependent on the number of characters.                                                                                    | No                              |                  
| `items.items[].item_specification_4`         | A separate field of the specification for the item produced by the business, the contents and order of this field can change dependent on the number of characters.                                                                                    | No                              |
| `items.items[].item_specification_5`         | A separate field of the specification for the item produced by the business, the contents and order of this field can change dependent on the number of characters.                                                                                    | No                              |
| `items.items[].unit_of_sale`                 | The unit of sale for the item produced bu the business                   | Yes                             |
| `items.items[].terms_of_sale_1`              | A separate field of the terms of sale for the item produced by the business, the contents and order of this field can change dependent on the number of characters.                                                                                    | No                              |                  
| `items.items[].terms_of_sale_2`              | A separate field of the terms of sale for the item produced by the business, the contents and order of this field can change dependent on the number of characters.                                                                                    | No                              |
| `items.items[].terms_of_sale_3`              | A separate field of the terms of sale for the item produced by the business, the contents and order of this field can change dependent on the number of characters.                                                                                    | No                              |
| `items.items[].terms_of_sale_4`              | A separate field of the terms of sale for the item produced by the business, the contents and order of this field can change dependent on the number of characters.                                                                                    | No                              |
| `items.items[].currency`                     | The currency which the product price is recorded in.                     | Yes                             |
| `items.items[].country_of_origin`            | The country of origin for the item                                       | Yes                             |


## Examples

Examples can be found at [examples/ipi](../examples/ipi).
