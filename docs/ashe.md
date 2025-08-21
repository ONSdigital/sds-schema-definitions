# SDS Unit Data Schema

This document describes the schema for the ASHE survey.

## Schema
  
v2 Template: [template_v2.json](/schemas/template_v2.json)

**The table below only describes data that is survey specific. The generic structure of supplementary data is documented in [README.md](README.md)**

| Path                                       | Description                                                                                                    | Mandatory |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------|-----------|
| `identifier`                               | The unique top-level identifier. This is a string representing the reporting unit reference.                   | Yes |
| `serial_number`                            | Unique person level identifier that ONS produce. | Yes |
| `employee_name`                            | The employee name. | Yes|
| `national_insurance_number_starred`        | The national insurance number of the employee, hidden by stars and only '14' revealed or 9 stars if its temporary or blank national number. | Yes |
| `work_id`                                  | The work number, branch and department. This field will appear blank if missing. | No |
| `work_postcode`                            | The employees work postcode. If missing (XX9 9XX) 'NOT KNOWN' will be displayed. | No |
| `home_postcode`                            | The employees work postcode. If missing (XX9 9XX) 'NOT KNOWN' will be displayed. | No |

## Examples

Examples can be found at [examples/ashe](../examples/ashe).
