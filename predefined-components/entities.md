# Entities

> An [_entity_](../core-concepts-and-definitions.md#entity) is any singular, identifiable, and separate object. It can refer to individuals, organizations, systems, pieces of data, or even distinct system components that are considered significant in and of themselves. In the context of OnePass, an entity refers to individual things, including people, concepts, or objects with data that is first stored in a database. Entities have [_attributes_](../core-concepts-and-definitions.md#entity-attributes) and _relationships_ with other entities.
>
> **Example:** A _Shareholder_, who can be a person or an organization, is an entity that has a many-to-many relationship with 'Organization' entities. This means that a single Shareholder can be associated with multiple Organizations, and vice versa.

<details>

<summary>About attributes</summary>

The _attributes_ of an entity are its characteristics or traits that describe the entity. For example, the _Shareholder>Person_ entity type has the following attributes:

* `type`: String ("person")
* `full_name`: String
* `role`: Array of Strings (e.g. \["director", "shareholder", "other"])
* `birth_date`: Date
* `ownership_percentage`: Number

</details>

The following table lists the predefined entities.  You can combine this entities to build you own verification types and levels, depending on your needs.

If you need to define a new entity not covered by this list, please follow the "[Creating new entities and objects](../guides/creating-new-entities-and-objects.md)" guide to create your own entities and objects or customize the existing ones.



<table data-full-width="true"><thead><tr><th>Type</th><th>Attributes</th><th>Schema definition</th><th>Schema preview</th></tr></thead><tbody><tr><td>Person (KYC)</td><td>First name, last name, birth date, country, ID document  </td><td><a href="https://crm-testbed.getonepass.eu/schemas/5d9717da21d742ea9e6a653c/builder">Schema</a></td><td><a href="https://crm-testbed.getonepass.eu/f/5d9717da21d742ea9e6a653c">Live preview</a></td></tr><tr><td>Person (team member)</td><td>Full name, position, country, bio, linkedin profile</td><td><a href="https://crm-testbed.getonepass.eu/schemas/9a2f18cd447b7dccc95a9230/builder">Schema</a></td><td><a href="https://crm-testbed.getonepass.eu/f/9a2f18cd447b7dccc95a9230">Live preview</a></td></tr><tr><td>Person (representative)</td><td>Name, type of representation, power of attorney</td><td><a href="https://crm-testbed.getonepass.eu/schemas/ccbc957c9a0ef9da9eae9aff/builder">Schema</a></td><td><a href="https://crm-testbed.getonepass.eu/f/ccbc957c9a0ef9da9eae9aff">Live preview</a></td></tr><tr><td>Person (UBO/Shareholder/Director)</td><td>Full name, role, nationality, date of birth, percentage of ownership/voting rights</td><td><a href="https://crm-testbed.getonepass.eu/schemas/3d73fc5a3c706279be6fa3d7/builder">Schema</a></td><td><a href="https://crm-testbed.getonepass.eu/f/3d73fc5a3c706279be6fa3d7">Live preview</a></td></tr><tr><td>Organization</td><td>Legal name, legal form, registration number, VAT/Tax number, incorporation date, country, address, sector/domain</td><td>N/A</td><td>N/A</td></tr><tr><td>Organization (Linked/Partner/Shareholder)</td><td>Full legal name, registration number, relationship, percentage of ownership, percentage of voting rights, country, financial statement</td><td><a href="https://crm-testbed.getonepass.eu/schemas/7df338d498de17d061fa88c2/builder">Schema</a></td><td><a href="https://crm-testbed.getonepass.eu/f/7df338d498de17d061fa88c2">Live preview</a></td></tr></tbody></table>



### Additional objects/schemas

<table data-full-width="true"><thead><tr><th>Type</th><th>Attributes</th><th>Schema definition</th><th>Schema preview</th></tr></thead><tbody><tr><td>Address</td><td>Country, city/locality, region/state/province, postal code, street name an number</td><td><a href="https://crm-testbed.getonepass.eu/schemas/ff080a9bbe3f5a6ff55e216a/builder">Schema</a></td><td><a href="https://crm-testbed.getonepass.eu/f/ff080a9bbe3f5a6ff55e216a">Live preview</a></td></tr><tr><td>Financial statement (basic)</td><td>Staff headcount, annual turnover, annual balance sheet total</td><td><a href="https://crm-testbed.getonepass.eu/schemas/10df3dd3032f72807ec8f894">Schema</a></td><td><a href="https://crm-testbed.getonepass.eu/f/10df3dd3032f72807ec8f894">Live preview</a></td></tr><tr><td>Financial statement (complete)</td><td>Capital, reserves, accumulated losses, short-term liabilities, long-term liabilities</td><td><a href="https://crm-testbed.getonepass.eu/schemas/efda7e3445558f12863b667c">Schema</a> </td><td><a href="https://crm-testbed.getonepass.eu/f/efda7e3445558f12863b667c">Live preview</a></td></tr><tr><td>Financial statement (FSTP)</td><td>All of the basic and complete financial statements plus additional questions related to financial issues, such as aids, insolvencies, and other financial concerns.</td><td><a href="https://crm-testbed.getonepass.eu/schemas/f4aabd3b1986af0d46ca1688">Schema</a></td><td><a href="https://crm-testbed.getonepass.eu/f/f4aabd3b1986af0d46ca1688">Live preview</a></td></tr><tr><td>ID document</td><td>Document type, document</td><td><a href="https://crm-testbed.getonepass.eu/schemas/7cd0690611d3345ffac98688/builder">Schema</a></td><td><a href="https://crm-testbed.getonepass.eu/f/7cd0690611d3345ffac98688">Live preview</a></td></tr></tbody></table>
