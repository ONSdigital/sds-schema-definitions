# Prodcom Survey SDS Schema

This document describes the schema for the ipi survey.

## Schema

Schema v1: [v1.json](/schemas/ipi/v1.json)

**The table below only describes data that is survey specific. The generic structure of supplementary data is documented in [README.md](/docs/README.md)**

| Path                                         | Description                                                              | Mandatory                       |
|----------------------------------------------|--------------------------------------------------------------------------|---------------------------------|
| `identifier`                                 | The unique top-level identifier. For business surveys this is the reporting unit reference without the check letter appended. In the final sel file, the RU REF is changed, If the first digit of an RU number is a 4 is the ref is changed to a 2 and if the first digit of the RU is a 5 the ref is changed to a 3                                                                                                                    | Yes                             |
| `supplier_number`                            | Like ruref, this is also a unique top-level identifier fo the business. The Supplier ID is essentially the RU number but the first digit is changed for  IPI. If the first digit is a 4 it is changed to a 2 and if the first digit of the is a 5 it is changed to a 3                                                                                                                         | Yes                             |
| `current_month`                              | The month and year that the data is required for.                        | Yes                             |
| `items`                                      | An object of items provided                                              | Yes                             |
| `items.item`                                 | The data about each item                                                 | Yes                             |
| `items.item.identifier`                      | The 10 digit unique reference for each item produced by the business. This number is allocated by ONS, if the item was to change the number would stay the same.                                                                                    | Yes                             |
| `items.items[].item_number`                  | The 10 digit unique reference for each item produced by the business. This number is allocated by ONS, if the item was to change the number would stay the same.                                                                                    | Yes                             |
| `items.items[].item_specification_1`         | A separate field of the specification for the item produced by the business, the contents and order of this field can change dependent on the number of characters. This line is always PRODUCT.                                                       | Yes                             |
| `items.items[].item_specification_2`         | A separate field of the specification for the item produced by the business, the contents and order of this field can change dependent on the number of characters.                                                                                    | No                              |
| `items.items[].item_specification_3`         | A separate field of the specification for the item produced by the business, the contents and order of this field can change dependent on the number of characters.                                                                                    | No                              |                  
| `items.items[].item_specification_4`         | A separate field of the specification for the item produced by the business, the contents and order of this field can change dependent on the number of characters.                                                                                    | No                              |
| `items.items[].item_specification_5`         | A separate field of the specification for the item produced by the business, the contents and order of this field can change dependent on the number of characters.                                                                                    | No                              |
| `items.items[].unit_of_sale`                 | The unit of sale for the item produced by the business                   | Yes                             |
| `items.items[].terms_of_sale_1`              | A separate field of the terms of sale for the item produced by the business, the contents and order of this field can change dependent on the number of characters.                                                                                    | Yes                             |                  
| `items.items[].terms_of_sale_2`              | A separate field of the terms of sale for the item produced by the business, the contents and order of this field can change dependent on the number of characters.                                                                                    | No                              |
| `items.items[].terms_of_sale_3`              | A separate field of the terms of sale for the item produced by the business, the contents and order of this field can change dependent on the number of characters.                                                                                    | No                              |
| `items.items[].terms_of_sale_4`              | A separate field of the terms of sale for the item produced by the business, the contents and order of this field can change dependent on the number of characters.                                                                                    | No                              |
| `items.items[].currency`                     | The currency for the item.                                               | Yes                             |
| `items.items[].country_of_origin`            | The country of origin for the item                                       | Yes                             |


## Examples

Examples can be found at [examples/ipi](../examples/ipi).
