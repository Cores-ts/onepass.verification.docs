---
description: >-
  This documents describes the core concepts and definitions used when
  implementing a verification service in OnePass.
---

# Core Concepts and definitions

### Applicant

An applicant can be either a _physical person_ or a _legal entity/organization_ that undergoes a verification process. By default, applicants must create their own account to initiate the verification process. However, you also have the option to manually create applicants one at a time by filling out a form or in bulk by importing a CSV or Excel file.

Information for each applicant is stored as a single record or a group of records across related processes.

### Entity

An _entity_ is any singular, identifiable, and separate object. It can refer to individuals, organizations, systems, pieces of data, or even distinct system components that are considered significant in and of themselves. In the context of OnePass, an entity refers to individual things, including people, concepts, or objects with data that is first stored in a database. Entities have _attributes_ and _relationships_ with other entities.

**Example:** A _Shareholder_, who can be a person or an organization, is an entity that has a many-to-many relationship with 'Organization' entities. This means that a single Shareholder can be associated with multiple Organizations, and vice versa.

#### Entity Attributes

The _attributes_ of an entity are its characteristics or traits that describe the entity.&#x20;

For example, the _Shareholder>Person_ entity has the following attributes:

<table data-full-width="true"><thead><tr><th>Attribute key</th><th>Attribute label</th><th>Attribute type</th><th data-type="checkbox">Required</th><th>Allowed values</th></tr></thead><tbody><tr><td>full_name</td><td>Full name</td><td>String</td><td>true</td><td>-</td></tr><tr><td>role</td><td>Role</td><td>Array of strings</td><td>true</td><td>Director, Shareholder, Other</td></tr><tr><td>birth_date</td><td>Birth date</td><td>Date</td><td>true</td><td>-</td></tr><tr><td>ownership_percentage</td><td>Ownership percentage</td><td>Number</td><td>true</td><td>-</td></tr></tbody></table>

### Record

A _record_ is the storage representation of a row of data.

### Verification flow

A verification flow is a sequence of steps that an applicant has to take to verify their identity. The verification flow is initiated when a verification request is sent by or to an applicant. The verification flow is completed when all verification checks have been performed.

The verification flow can be customized to include different verification levels and checks, depending on your scenario and how you want your applicants to be verified. For example, you can create a region-based flow that requests one set of documents in low-risk regions and a different set of documents in high-risk regions.

When referring to data collection, the data can be collected by a standalone form or by a sequence of forms. The sequence of forms is called a flow.

When using a standalone form, all the data is collected in a single step. When using a flow, the data is collected in multiple steps that maybe be automatically triggered based in conditions or user actions.

### Verification request

A verification request is a request to verify an applicant's identity. You can create a verification request for an applicant by selecting the verification levels you want to include and then sending the request to the applicant.

### Verification agent

Verification agents are individuals responsible for verifying the identity of applicants by performing verification checks. They are also responsible for updating the status of verification checks and verification levels.

The verification agent is responsible for verifying

* the applicant's identity
* the applicant's documents
* the applicant's information ...

### Verification type

A verification type refers to a particular kind of examination you wish to conduct on an applicant, based on your compliance or diligence requirements. For instance, you can establish a verification type for specific data such as the applicant legal information, shareholders or the financial status.

By combining various verification types, you can create intricate verification levels tailored to your specific scenario.

### Verification check

A verification check is a single task carried out by verification agents in the process of verification. Each check is defined to confirm or validate a specific detail or document.

### Verification level

A level is a collection of verifications that you need to perform on your applicants based on your scenario.

Basically, a level defines the data that needs to be collected from an applicant and the consequent checks the applicant needs to pass.

### Verification result

A verification result is the outcome of a verification check. The result can be one of the following:

* **Approved** – The user has passed the verification check.
* **Rejected** – The user has failed the verification check.

### Verification status

The verification status is the current state of the verification process. The status can be one of the following:

* **Pending** – The verification process is still in progress.
* **Approved** – The verification process has been completed and the user has passed all verification checks.
* **Rejected** – The verification process has been completed and the user has failed one or more verification checks.

### Ultimate beneficial owner (UBO)

Ultimate beneficial owners (UBOs) are the natural persons who directly or indirectly own or exercise control over **more than 25%** of a organization's shares or voting rights. This includes directors and any individual who holds the power to appoint or remove a majority of the board of directors or to influence or control the organization's policies or management.

In cases where an organization's owner is a legal entity, such as a trust or holding company, the owner of that legal entity is also considered a UBO.

_**Example**: If a natural person owns 60% of Organization A, and Organization A owns 50% of Organization B, then the natural person is a beneficial owner of Organization B with a percentage of ownership equal to 30% (60% \* 50%)._

### Shareholder

A shareholder is a natural person or legal entity that legally owns **one or more** shares of a company's stock. Shareholders are the owners of a company.

### Company authorized representative

A company authorized representative is a person who is authorized to act on behalf of a company. This person can be a director, a shareholder, or any other person who has been given the authority to act on behalf of the company.

### SME

A small or medium-sized enterprise (SME) is a company that has a limited number of employees and a limited amount of revenue. The exact definition of an SME can vary depending on the country and the industry, but it is generally used to refer to companies that are smaller than large corporations.

EU-definition References:

* https://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32003H0361\&rid=5
* https://ec.europa.eu/docsroom/documents/42921

### Associated company

An associated company is a company that is related to another company in some way. This can include companies that are part of the same group, companies that are owned by the same person, or companies that have some other kind of relationship.

### Enterprise

Any entity involved in economic activities, regardless of its legal structure. The key factor is the engagement in economic activities, not the legal form.

Therefore, self-employed individuals, family businesses, partnerships, associations, or any other entity that regularly participates in economic activities can be classified as enterprises.

### Autonomous enterprise

An autonomous enterprise is a company that operates independently, with minimal external partnerships. This typically means that no single enterprise owns more than 25% of the company's shares or voting rights.

**Exceptions to the 25% Rule**

There are certain types of investors that are exempt from the 25% rule, and an enterprise may still be considered autonomous even if the threshold is reached or exceeded by these investors:

* Public investment corporations, venture capital companies, and business angels
* Universities and non-profit research centers
* Institutional investors, such as regional development funds
* Autonomous local authorities with an annual budget of less than EUR 10 million and a population of fewer than 5,000 inhabitants

An enterprise may have one or more of these exempt investors, and they may individually hold up to 50% of the enterprise's shares. However, these investors must not be associated with the enterprise being assessed under SME guidelines.

### Partner enterprise

An enterprise that has holdings with other enterprises ranging from 25% to 50%.

### Linked enterprise

An enterprise that has holdings with other enterprises that exceed the 50% threshold.

### Parent and Child (Downstream/Upstream) enterprises

* An "upstream" enterprise, or parent enterprise, is a company that has ownership, partial ownership, or controlling interest in another enterprise.
* A "downstream" enterprise, or child enterprise, is a company that is owned, partially owned, or controlled by another enterprise.

### Staff headcount

The staff headcount includes both permanent and temporary personnel, and encompasses the following:

* Employees
* Seconded personnel who are considered employees under national law (this may include interim or temporary staff)
* Owner-managers
* Partners who regularly engage in enterprise activities and derive financial benefits from it.

**Exclusions from staff headcount:**

* Apprentices or students engaged in vocational training with apprenticeship or vocational training contracts.
* Employees on maternity or parental leave.

### Annual turnover

Annual turnover is determined by calculating the income that an enterprise received during the year in question from the sale of products and provision of services falling within the company’s ordinary activities, after deducting any rebates. Turn- over should not include value added tax (VAT) or other indirect taxes.

### Annual balance sheet total

The annual balance sheet total refers to the value of a company’s main assets.
