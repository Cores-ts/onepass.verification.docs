# Creating new entities and objects

### Defining custom attributes for entities

You can define custom attributes for entities by creating a new schema. This allows you to add new fields to the entity that are specific to your use case. If you need additional information that is not included in the predefined entities, you can create a new schema and add the fields you need. For example, you can add fields for the organization's industry, the number of employees, or the annual turnover.

### Defining custom entities

If you need to define a new entity not covered by the predefined entities, you can create a new schema and add the fields you need. For example, you can create a new entity for a specific type of organization, such as a non-profit organization, or a specific type of person, such as a freelancer. To define a new entity type, follow these steps:

1. Create a new JSON file in the `schemas` directory. The filename should be the name of the new entity type, in lowercase, with the `.json` extension. For example, if you want to create a new entity type called "freelancer", create a file called `freelancer.json`.
2. Add the fields you need to the new schema. For example, you can add fields for the freelancer's skills, experience, and portfolio.
3. Add the new entity type to the `entities` array in the `schemas.json` file. For example, if you created a new entity type called "freelancer", add `"freelancer"` to the `entities` array.
