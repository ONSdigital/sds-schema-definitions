# ASHE Survey SDS Schema

This document describes the schema for the ASHE survey.

## Schema

Schema: [v1.json](/schemas/ashe/v1.json)

**The table below only describes data that is survey specific. The generic structure of supplementary data is documented in [README.md](README.md)**

| Path                                                 | Description                                                                                                                                            | Mandatory |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| `identifier`                                         | ASHE_RU to be used which mimics a RUREF. Format is surveyID (141), zeros, followed by an incrementing count. Must count to 11 digits.                  | Yes       |
| `items`                                              | An object of items provided.                                                                                                                           | Yes       |
| `items.employee[]`                                   | The data about each item.                                                                                                                              | Yes       |
| `items.employee[].identifier`                        | The unique person level identifier that the ONS produces                                                                                               | Yes       |
| `items.employee[].employee_name`                     | The employee name                                                                                                                                      | Yes       |
| `items.employee[].national_insurance_number_starred` | The national insurance number of the employee, hidden by stars and only '14' revealed or 9 stars if its a temporary or blank national insurance number | Yes       |
| `items.employee[].work_id`                           | The work number, branch and department. This field will appear blank if missing.                                                                       | No        |
| `items.employee[].work_postcode`                     | The employees work postcode. If missing (XX9 9XX), 'NOT KNOWN' will be displayed.                                                                      | No        |
| `items.employee[].home_postcode`                     | The employees home postcode. If missing (XX9 9XX), 'NOT KNOWN' will be displayed.                                                                      | No        |



## Examples

Examples can be found at [examples/ashe](../examples/ashe).