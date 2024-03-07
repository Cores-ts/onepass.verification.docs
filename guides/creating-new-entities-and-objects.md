# Creating new entities and objects

### Defining custom entities

If you need to define a new entity not covered by the predefined entities, you can create a new schema and add the fields you need. For example, you can create a new entity for a specific type of organization, such as a non-profit organization, or a specific type of person, such as a freelancer. To define a new entity type, follow these steps:

1. **Choose a Name for Your Entity**: Start by deciding on a unique name that clearly represents your entity. This name will be used to reference your entity in your database and application code.
2. **Define Your Fields**: Determine what information you need to store for your entity. Each piece of information will be a field in your schema. Common fields for an organization might include `name`, `address`, `phone_number`, and `type_of_organization`.
3. **Specify Field Types**: For each field, specify the type of data it will hold. Common data types include `string` for text, `number` for numerical values, and `date` for date and time information.
4. **Set Required Fields**: Decide which fields are mandatory for your entity. These required fields must be filled out for an entity to be considered valid in your system.
5. **Create Relationships (Optional)**: If your entity is related to other entities in the system, define those relationships. For instance, a `freelancer` might be linked to `projects`, and a `non-profit organization` might be linked to `donors`.

**Example Schema for a Non-Profit Organization Entity:**

```plaintext
Entity Name: NonProfitOrganization
Fields:
- name (string, required)
- address (string, required)
- phone_number (string, optional)
- type_of_organization (string, required, default="Non-Profit")
- founded_date (date, optional)
- mission_statement (string, optional)
Relationships:
- donors (Many-to-One)
```

6. **Test Your Entity**: Finally, create test cases to ensure that your entity behaves as expected. Pay special attention to required fields and relationships.

Visual guide (pending)

