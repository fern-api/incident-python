# Reference
## Actions V1
<details><summary><code>client.actions_v1.<a href="src/fern/actions_v1/client.py">list</a>(...) -&gt; AsyncHttpResponse[ActionsListResultV1]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List all actions for an organisation.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.actions_v1.list(
    incident_id="01FCNDV6P870EA6S7TK1DSYDG0",
    is_follow_up=True,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**incident_id:** `typing.Optional[str]` — Find actions related to this incident
    
</dd>
</dl>

<dl>
<dd>

**is_follow_up:** `typing.Optional[bool]` — Filter to actions marked as being follow up actions
    
</dd>
</dl>

<dl>
<dd>

**incident_mode:** `typing.Optional[ActionsV1ListRequestIncidentMode]` — Filter to actions from incidents of the given mode. If not set, only actions from `real` incidents are returned
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.actions_v1.<a href="src/fern/actions_v1/client.py">show</a>(...) -&gt; AsyncHttpResponse[ActionsShowResultV1]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a single incident action.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.actions_v1.show(
    id="01FCNDV6P870EA6S7TK1DSYDG0",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — Unique identifier for the action
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Custom Field Options V1
<details><summary><code>client.custom_field_options_v1.<a href="src/fern/custom_field_options_v1/client.py">list</a>(...) -&gt; AsyncHttpResponse[CustomFieldOptionsListResultV1]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Show custom field options for a custom field
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.custom_field_options_v1.list(
    page_size=25,
    after="01G0J1EXE7AXZ2C93K61WBPYEH",
    custom_field_id="01FCNDV6P870EA6S7TK1DSYD5H",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**custom_field_id:** `str` — The custom field to list options for.
    
</dd>
</dl>

<dl>
<dd>

**page_size:** `typing.Optional[int]` — Integer number of records to return
    
</dd>
</dl>

<dl>
<dd>

**after:** `typing.Optional[str]` — A custom field option's ID. This endpoint will return a list of custom field options created after this option.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.custom_field_options_v1.<a href="src/fern/custom_field_options_v1/client.py">create</a>(...) -&gt; AsyncHttpResponse[CustomFieldOptionsCreateResultV1]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a custom field option. If the sort key is not supplied, it'll default to 1000, so the option appears near the end of the list.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.custom_field_options_v1.create(
    custom_field_id="01FCNDV6P870EA6S7TK1DSYDG0",
    sort_key=10,
    value="Product",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**custom_field_id:** `str` — ID of the custom field this option belongs to
    
</dd>
</dl>

<dl>
<dd>

**value:** `str` — Human readable name for the custom field option
    
</dd>
</dl>

<dl>
<dd>

**sort_key:** `typing.Optional[int]` — Sort key used to order the custom field options correctly
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.custom_field_options_v1.<a href="src/fern/custom_field_options_v1/client.py">show</a>(...) -&gt; AsyncHttpResponse[CustomFieldOptionsShowResultV1]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a single custom field option
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.custom_field_options_v1.show(
    id="01FCNDV6P870EA6S7TK1DSYDG0",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — Unique identifier for the custom field option
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.custom_field_options_v1.<a href="src/fern/custom_field_options_v1/client.py">update</a>(...) -&gt; AsyncHttpResponse[CustomFieldOptionsUpdateResultV1]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update a custom field option
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.custom_field_options_v1.update(
    id="01FCNDV6P870EA6S7TK1DSYDG0",
    sort_key=10,
    value="Product",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — Unique identifier for the custom field option
    
</dd>
</dl>

<dl>
<dd>

**sort_key:** `int` — Sort key used to order the custom field options correctly
    
</dd>
</dl>

<dl>
<dd>

**value:** `str` — Human readable name for the custom field option
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.custom_field_options_v1.<a href="src/fern/custom_field_options_v1/client.py">delete</a>(...) -&gt; AsyncHttpResponse[None]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete a custom field option
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.custom_field_options_v1.delete(
    id="01FCNDV6P870EA6S7TK1DSYDG0",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — Unique identifier for the custom field option
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Custom Fields V1
<details><summary><code>client.custom_fields_v1.<a href="src/fern/custom_fields_v1/client.py">list</a>() -&gt; AsyncHttpResponse[CustomFieldsListResultV1]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List all custom fields for an organisation.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.custom_fields_v1.list()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.custom_fields_v1.<a href="src/fern/custom_fields_v1/client.py">create</a>(...) -&gt; AsyncHttpResponse[CustomFieldsCreateResultV1]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new custom field
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.custom_fields_v1.create(
    description="Which team is impacted by this issue",
    field_type="single_select",
    name="Affected Team",
    required="never",
    required_v2="never",
    show_before_closure=True,
    show_before_creation=True,
    show_before_update=True,
    show_in_announcement_post=True,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**description:** `str` — Description of the custom field
    
</dd>
</dl>

<dl>
<dd>

**field_type:** `CustomFieldsCreatePayloadV1FieldType` — Type of custom field
    
</dd>
</dl>

<dl>
<dd>

**name:** `str` — Human readable name for the custom field
    
</dd>
</dl>

<dl>
<dd>

**show_before_closure:** `bool` — Whether a custom field should be shown in the incident resolve modal. If this custom field is required before resolution, but no value has been set for it, the field will be shown in the resolve modal whatever the value of this setting.
    
</dd>
</dl>

<dl>
<dd>

**show_before_creation:** `bool` — Whether a custom field should be shown in the incident creation modal. This must be true if the field is always required.
    
</dd>
</dl>

<dl>
<dd>

**show_before_update:** `bool` — Whether a custom field should be shown in the incident update modal.
    
</dd>
</dl>

<dl>
<dd>

**required:** `typing.Optional[CustomFieldsCreatePayloadV1Required]` — When this custom field must be set during the incident lifecycle. [DEPRECATED: please use required_v2 instead].
    
</dd>
</dl>

<dl>
<dd>

**required_v2:** `typing.Optional[CustomFieldsCreatePayloadV1RequiredV2]` — When this custom field must be set during the incident lifecycle.
    
</dd>
</dl>

<dl>
<dd>

**show_in_announcement_post:** `typing.Optional[bool]` — Whether a custom field should be shown in the list of fields as part of the announcement post when set.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.custom_fields_v1.<a href="src/fern/custom_fields_v1/client.py">show</a>(...) -&gt; AsyncHttpResponse[CustomFieldsShowResultV1]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a single custom field.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.custom_fields_v1.show(
    id="01FCNDV6P870EA6S7TK1DSYDG0",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — Unique identifier for the custom field
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.custom_fields_v1.<a href="src/fern/custom_fields_v1/client.py">update</a>(...) -&gt; AsyncHttpResponse[CustomFieldsUpdateResultV1]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update the details of a custom field
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.custom_fields_v1.update(
    id="01FCNDV6P870EA6S7TK1DSYDG0",
    description="Which team is impacted by this issue",
    name="Affected Team",
    required="never",
    required_v2="never",
    show_before_closure=True,
    show_before_creation=True,
    show_before_update=True,
    show_in_announcement_post=True,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — Unique identifier for the custom field
    
</dd>
</dl>

<dl>
<dd>

**description:** `str` — Description of the custom field
    
</dd>
</dl>

<dl>
<dd>

**name:** `str` — Human readable name for the custom field
    
</dd>
</dl>

<dl>
<dd>

**show_before_closure:** `bool` — Whether a custom field should be shown in the incident resolve modal. If this custom field is required before resolution, but no value has been set for it, the field will be shown in the resolve modal whatever the value of this setting.
    
</dd>
</dl>

<dl>
<dd>

**show_before_creation:** `bool` — Whether a custom field should be shown in the incident creation modal. This must be true if the field is always required.
    
</dd>
</dl>

<dl>
<dd>

**show_before_update:** `bool` — Whether a custom field should be shown in the incident update modal.
    
</dd>
</dl>

<dl>
<dd>

**required:** `typing.Optional[CustomFieldsUpdatePayloadV1Required]` — When this custom field must be set during the incident lifecycle. [DEPRECATED: please use required_v2 instead].
    
</dd>
</dl>

<dl>
<dd>

**required_v2:** `typing.Optional[CustomFieldsUpdatePayloadV1RequiredV2]` — When this custom field must be set during the incident lifecycle.
    
</dd>
</dl>

<dl>
<dd>

**show_in_announcement_post:** `typing.Optional[bool]` — Whether a custom field should be shown in the list of fields as part of the announcement post when set.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.custom_fields_v1.<a href="src/fern/custom_fields_v1/client.py">delete</a>(...) -&gt; AsyncHttpResponse[None]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete a custom field
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.custom_fields_v1.delete(
    id="01FCNDV6P870EA6S7TK1DSYDG0",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — Unique identifier for the custom field
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Utilities V1
<details><summary><code>client.utilities_v1.<a href="src/fern/utilities_v1/client.py">identity</a>() -&gt; AsyncHttpResponse[UtilitiesIdentityResultV1]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Test if your API key is valid, and which roles it has.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.utilities_v1.identity()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Incident Attachments V1
<details><summary><code>client.incident_attachments_v1.<a href="src/fern/incident_attachments_v1/client.py">list</a>(...) -&gt; AsyncHttpResponse[IncidentAttachmentsListResultV1]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List all incident attachments for a given external resource or incident. You must provide either a specific incident ID or a specific external resource type and external ID.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.incident_attachments_v1.list(
    incident_id="01G0J1EXE7AXZ2C93K61WBPYEH",
    external_id="123",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**incident_id:** `typing.Optional[str]` — Incident that this attachment is against
    
</dd>
</dl>

<dl>
<dd>

**external_id:** `typing.Optional[str]` — ID of the resource in the external system
    
</dd>
</dl>

<dl>
<dd>

**resource_type:** `typing.Optional[IncidentAttachmentsV1ListRequestResourceType]` — E.g. PagerDuty: the external system that holds the resource
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.incident_attachments_v1.<a href="src/fern/incident_attachments_v1/client.py">create</a>(...) -&gt; AsyncHttpResponse[IncidentAttachmentsCreateResultV1]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Attaches an external resource to an incident
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern.incident_attachments_v1 import (
    IncidentAttachmentsCreatePayloadV1Resource,
)

from fern import IncidentIO

client = IncidentIO()
client.incident_attachments_v1.create(
    incident_id="01FDAG4SAP5TYPT98WGR2N7W91",
    resource=IncidentAttachmentsCreatePayloadV1Resource(
        external_id="123",
        resource_type="pager_duty_incident",
    ),
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**incident_id:** `str` — ID of the incident to add an attachment to
    
</dd>
</dl>

<dl>
<dd>

**resource:** `IncidentAttachmentsCreatePayloadV1Resource` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.incident_attachments_v1.<a href="src/fern/incident_attachments_v1/client.py">delete</a>(...) -&gt; AsyncHttpResponse[None]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Unattaches an external resource from an incident
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.incident_attachments_v1.delete(
    id="01FCNDV6P870EA6S7TK1DSYD5H",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — Unique identifier of this incident membership
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Incident Memberships V1
<details><summary><code>client.incident_memberships_v1.<a href="src/fern/incident_memberships_v1/client.py">create</a>(...) -&gt; AsyncHttpResponse[IncidentMembershipsCreateResultV1]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Makes a user a member of a private incident
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.incident_memberships_v1.create(
    incident_id="01ET65M7ZADYFCKD4K1AE2QNMC",
    user_id="01FCQSP07Z74QMMYPDDGQB9FTG",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**incident_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.incident_memberships_v1.<a href="src/fern/incident_memberships_v1/client.py">revoke</a>(...) -&gt; AsyncHttpResponse[None]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Revoke a user's membership of a private incident
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.incident_memberships_v1.revoke(
    incident_id="01FCNDV6P870EA6S7TK1DSYD5H",
    user_id="01FCQSP07Z74QMMYPDDGQB9FTG",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**incident_id:** `str` — Revoke memberships to incident
    
</dd>
</dl>

<dl>
<dd>

**user_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Incident Relationships V1
<details><summary><code>client.incident_relationships_v1.<a href="src/fern/incident_relationships_v1/client.py">list</a>(...) -&gt; AsyncHttpResponse[IncidentRelationshipsListResultV1]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List related incidents for a specific incident.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.incident_relationships_v1.list(
    incident_id="01FCNDV6P870EA6S7TK1DSYD5H",
    page_size=25,
    after="01FDAG4SAP5TYPT98WGR2N7W91",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**incident_id:** `str` — ID of the incident to find relationships for
    
</dd>
</dl>

<dl>
<dd>

**page_size:** `typing.Optional[int]` — Integer number of records to return
    
</dd>
</dl>

<dl>
<dd>

**after:** `typing.Optional[str]` — An record's ID. This endpoint will return a list of records after this ID in relation to the API response order.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Incident Roles V1
<details><summary><code>client.incident_roles_v1.<a href="src/fern/incident_roles_v1/client.py">list</a>() -&gt; AsyncHttpResponse[IncidentRolesListResultV1]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List all incident roles for an organisation.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.incident_roles_v1.list()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.incident_roles_v1.<a href="src/fern/incident_roles_v1/client.py">create</a>(...) -&gt; AsyncHttpResponse[IncidentRolesCreateResultV1]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new incident role
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.incident_roles_v1.create(
    description="The person currently coordinating the incident",
    instructions="Take point on the incident; Make sure people are clear on responsibilities",
    name="Incident Lead",
    required=False,
    shortform="lead",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**description:** `str` — Describes the purpose of the role
    
</dd>
</dl>

<dl>
<dd>

**instructions:** `str` — Provided to whoever is nominated for the role. Note that this will be empty for the 'reporter' role.
    
</dd>
</dl>

<dl>
<dd>

**name:** `str` — Human readable name of the incident role
    
</dd>
</dl>

<dl>
<dd>

**required:** `bool` — DEPRECATED: this will always be false.
    
</dd>
</dl>

<dl>
<dd>

**shortform:** `str` — Short human readable name for Slack. Note that this will be empty for the 'reporter' role.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.incident_roles_v1.<a href="src/fern/incident_roles_v1/client.py">show</a>(...) -&gt; AsyncHttpResponse[IncidentRolesShowResultV1]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a single incident role.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.incident_roles_v1.show(
    id="01FCNDV6P870EA6S7TK1DSYDG0",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — Unique identifier for the role
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.incident_roles_v1.<a href="src/fern/incident_roles_v1/client.py">update</a>(...) -&gt; AsyncHttpResponse[IncidentRolesUpdateResultV1]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update an existing incident role
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.incident_roles_v1.update(
    id="01FCNDV6P870EA6S7TK1DSYDG0",
    description="The person currently coordinating the incident",
    instructions="Take point on the incident; Make sure people are clear on responsibilities",
    name="Incident Lead",
    required=False,
    shortform="lead",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — Unique identifier for the role
    
</dd>
</dl>

<dl>
<dd>

**description:** `str` — Describes the purpose of the role
    
</dd>
</dl>

<dl>
<dd>

**instructions:** `str` — Provided to whoever is nominated for the role. Note that this will be empty for the 'reporter' role.
    
</dd>
</dl>

<dl>
<dd>

**name:** `str` — Human readable name of the incident role
    
</dd>
</dl>

<dl>
<dd>

**shortform:** `str` — Short human readable name for Slack. Note that this will be empty for the 'reporter' role.
    
</dd>
</dl>

<dl>
<dd>

**required:** `typing.Optional[bool]` — DEPRECATED: this will always be false.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.incident_roles_v1.<a href="src/fern/incident_roles_v1/client.py">delete</a>(...) -&gt; AsyncHttpResponse[None]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Removes an existing role
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.incident_roles_v1.delete(
    id="01FCNDV6P870EA6S7TK1DSYDG0",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — Unique identifier for the role
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Incident Statuses V1
<details><summary><code>client.incident_statuses_v1.<a href="src/fern/incident_statuses_v1/client.py">list</a>() -&gt; AsyncHttpResponse[IncidentStatusesListResultV1]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List all incident statuses for an organisation.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.incident_statuses_v1.list()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.incident_statuses_v1.<a href="src/fern/incident_statuses_v1/client.py">create</a>(...) -&gt; AsyncHttpResponse[IncidentStatusesCreateResultV1]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new incident status
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.incident_statuses_v1.create(
    category="live",
    description="Impact has been **fully mitigated**, and we're ready to learn from this incident.",
    name="Closed",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**category:** `IncidentStatusesCreatePayloadV1Category` — Whether the status should be considered 'live' (now renamed to active), 'learning' (now renamed to post-incident) or 'closed'. The triage and declined statuses cannot be created or modified.
    
</dd>
</dl>

<dl>
<dd>

**description:** `str` — Rich text description of the incident status
    
</dd>
</dl>

<dl>
<dd>

**name:** `str` — Unique name of this status
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.incident_statuses_v1.<a href="src/fern/incident_statuses_v1/client.py">show</a>(...) -&gt; AsyncHttpResponse[IncidentStatusesShowResultV1]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a single incident status.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.incident_statuses_v1.show(
    id="01FCNDV6P870EA6S7TK1DSYD5H",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — Unique ID of this incident status
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.incident_statuses_v1.<a href="src/fern/incident_statuses_v1/client.py">update</a>(...) -&gt; AsyncHttpResponse[IncidentStatusesUpdateResultV1]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update an existing incident status
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.incident_statuses_v1.update(
    id="01FCNDV6P870EA6S7TK1DSYD5H",
    description="Impact has been **fully mitigated**, and we're ready to learn from this incident.",
    name="Closed",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — Unique ID of this incident status
    
</dd>
</dl>

<dl>
<dd>

**description:** `str` — Rich text description of the incident status
    
</dd>
</dl>

<dl>
<dd>

**name:** `str` — Unique name of this status
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.incident_statuses_v1.<a href="src/fern/incident_statuses_v1/client.py">delete</a>(...) -&gt; AsyncHttpResponse[None]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete an incident status
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.incident_statuses_v1.delete(
    id="01FCNDV6P870EA6S7TK1DSYD5H",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — Unique ID of this incident status
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Incident Types V1
<details><summary><code>client.incident_types_v1.<a href="src/fern/incident_types_v1/client.py">list</a>() -&gt; AsyncHttpResponse[IncidentTypesListResultV1]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List all incident types for an organisation.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.incident_types_v1.list()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.incident_types_v1.<a href="src/fern/incident_types_v1/client.py">show</a>(...) -&gt; AsyncHttpResponse[IncidentTypesShowResultV1]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a single incident type.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.incident_types_v1.show(
    id="01FCNDV6P870EA6S7TK1DSYDG0",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — Unique identifier for this Incident Type
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Incidents V1
<details><summary><code>client.incidents_v1.<a href="src/fern/incidents_v1/client.py">list</a>(...) -&gt; AsyncHttpResponse[IncidentsListResultV1]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List all incidents for an organisation.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.incidents_v1.list(
    page_size=25,
    after="01FDAG4SAP5TYPT98WGR2N7W91",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**page_size:** `typing.Optional[int]` — Integer number of records to return
    
</dd>
</dl>

<dl>
<dd>

**after:** `typing.Optional[str]` — An record's ID. This endpoint will return a list of records after this ID in relation to the API response order.
    
</dd>
</dl>

<dl>
<dd>

**status:** `typing.Optional[typing.Union[str, typing.Sequence[str]]]` — Filter for incidents in these statuses
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.incidents_v1.<a href="src/fern/incidents_v1/client.py">create</a>(...) -&gt; AsyncHttpResponse[IncidentsCreateResultV1]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new incident.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import (
    CustomFieldEntryPayloadV1,
    CustomFieldValuePayloadV1,
    IncidentIO,
    IncidentRoleAssignmentPayloadV1,
    UserReferencePayloadV1,
)

client = IncidentIO()
client.incidents_v1.create(
    custom_field_entries=[
        CustomFieldEntryPayloadV1(
            custom_field_id="01FCNDV6P870EA6S7TK1DSYDG0",
            values=[
                CustomFieldValuePayloadV1(
                    id="01FCNDV6P870EA6S7TK1DSYDG0",
                    value_catalog_entry_id="01FCNDV6P870EA6S7TK1DSYDG0",
                    value_link="https://google.com/",
                    value_numeric="123.456",
                    value_option_id="01FCNDV6P870EA6S7TK1DSYDG0",
                    value_text="This is my text field, I hope you like it",
                    value_timestamp="",
                )
            ],
        )
    ],
    idempotency_key="alert-uuid",
    incident_role_assignments=[
        IncidentRoleAssignmentPayloadV1(
            assignee=UserReferencePayloadV1(
                email="bob@example.com",
                id="01G0J1EXE7AXZ2C93K61WBPYEH",
                slack_user_id="USER123",
            ),
            incident_role_id="01FH5TZRWMNAFB0DZ23FD1TV96",
        )
    ],
    incident_type_id="01FH5TZRWMNAFB0DZ23FD1TV96",
    mode="real",
    name="Our database is sad",
    severity_id="01FH5TZRWMNAFB0DZ23FD1TV96",
    slack_team_id="T02A1FSLE8J",
    source_message_channel_id="C02AW36C1M5",
    source_message_timestamp="1653650280.526509",
    status="triage",
    summary="Our database is really really sad, and we don't know why yet.",
    visibility="public",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**idempotency_key:** `str` — Unique string used to de-duplicate incident create requests
    
</dd>
</dl>

<dl>
<dd>

**visibility:** `IncidentsCreatePayloadV1Visibility` — Whether the incident should be open to anyone in your Slack workspace (public), or invite-only (private). For more information on Private Incidents see our [help centre](https://help.incident.io/articles/5905558102-can-we-mark-incidents-as-sensitive-and-restrict-access).
    
</dd>
</dl>

<dl>
<dd>

**custom_field_entries:** `typing.Optional[typing.Sequence[CustomFieldEntryPayloadV1]]` — Set the incident's custom fields to these values
    
</dd>
</dl>

<dl>
<dd>

**incident_role_assignments:** `typing.Optional[typing.Sequence[IncidentRoleAssignmentPayloadV1]]` — Assign incident roles to these people
    
</dd>
</dl>

<dl>
<dd>

**incident_type_id:** `typing.Optional[str]` — Incident type to create this incident as
    
</dd>
</dl>

<dl>
<dd>

**mode:** `typing.Optional[IncidentsCreatePayloadV1Mode]` — Whether the incident is real or test
    
</dd>
</dl>

<dl>
<dd>

**name:** `typing.Optional[str]` — Explanation of the incident
    
</dd>
</dl>

<dl>
<dd>

**severity_id:** `typing.Optional[str]` — Severity to create incident as
    
</dd>
</dl>

<dl>
<dd>

**slack_team_id:** `typing.Optional[str]` — ID of the Slack team / workspace. This is only required if you are using a Slack Enterprise Grid with multiple teams.
    
</dd>
</dl>

<dl>
<dd>

**source_message_channel_id:** `typing.Optional[str]` — Channel ID of the source message, if this incident was created from one
    
</dd>
</dl>

<dl>
<dd>

**source_message_timestamp:** `typing.Optional[str]` — Timestamp of the source message, if this incident was created from one
    
</dd>
</dl>

<dl>
<dd>

**status:** `typing.Optional[IncidentsCreatePayloadV1Status]` — Current status of the incident
    
</dd>
</dl>

<dl>
<dd>

**summary:** `typing.Optional[str]` — Detailed description of the incident
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.incidents_v1.<a href="src/fern/incidents_v1/client.py">show</a>(...) -&gt; AsyncHttpResponse[IncidentsShowResultV1]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a single incident.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.incidents_v1.show(
    id="01FDAG4SAP5TYPT98WGR2N7W91",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — Unique identifier for the incident
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## IPAllowlists V1
<details><summary><code>client.ipallowlists_v1.<a href="src/fern/ipallowlists_v1/client.py">showipallowlist</a>() -&gt; AsyncHttpResponse[IpAllowlistsShowIpAllowlistResultV1]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Show the IP allowlist for your organisation
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.ipallowlists_v1.showipallowlist()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ipallowlists_v1.<a href="src/fern/ipallowlists_v1/client.py">updateipallowlist</a>(...) -&gt; AsyncHttpResponse[IpAllowlistsUpdateIpAllowlistResultV1]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update the IP allowlist for your organisation
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO, IpAllowlistItemV1

client = IncidentIO()
client.ipallowlists_v1.updateipallowlist(
    allowlist=[
        IpAllowlistItemV1(
            label="London HQ",
            value="192.0.2.0",
        )
    ],
    enabled=True,
    version=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**allowlist:** `typing.Sequence[IpAllowlistItemV1]` — A list of IP addresses or CIDR prefixes to allow
    
</dd>
</dl>

<dl>
<dd>

**enabled:** `bool` — Whether this IP allowlist is enabled or not
    
</dd>
</dl>

<dl>
<dd>

**version:** `int` — The version of this IP allowlist
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Severities V1
<details><summary><code>client.severities_v1.<a href="src/fern/severities_v1/client.py">list</a>() -&gt; AsyncHttpResponse[SeveritiesListResultV1]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List all incident severities for an organisation.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.severities_v1.list()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.severities_v1.<a href="src/fern/severities_v1/client.py">create</a>(...) -&gt; AsyncHttpResponse[SeveritiesCreateResultV1]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new severity
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.severities_v1.create(
    description="Issues with **low impact**.",
    name="Minor",
    rank=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**description:** `str` — Description of the severity
    
</dd>
</dl>

<dl>
<dd>

**name:** `str` — Human readable name of the severity
    
</dd>
</dl>

<dl>
<dd>

**rank:** `typing.Optional[int]` — Rank to help sort severities (lower numbers are less severe)
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.severities_v1.<a href="src/fern/severities_v1/client.py">show</a>(...) -&gt; AsyncHttpResponse[SeveritiesShowResultV1]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a single incident severity.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.severities_v1.show(
    id="01FCNDV6P870EA6S7TK1DSYDG0",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — Unique identifier of the severity
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.severities_v1.<a href="src/fern/severities_v1/client.py">update</a>(...) -&gt; AsyncHttpResponse[SeveritiesUpdateResultV1]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update an existing severity
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.severities_v1.update(
    id="01FCNDV6P870EA6S7TK1DSYDG0",
    description="Issues with **low impact**.",
    name="Minor",
    rank=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — Unique identifier of the severity
    
</dd>
</dl>

<dl>
<dd>

**description:** `str` — Description of the severity
    
</dd>
</dl>

<dl>
<dd>

**name:** `str` — Human readable name of the severity
    
</dd>
</dl>

<dl>
<dd>

**rank:** `typing.Optional[int]` — Rank to help sort severities (lower numbers are less severe)
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.severities_v1.<a href="src/fern/severities_v1/client.py">delete</a>(...) -&gt; AsyncHttpResponse[None]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete a severity
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.severities_v1.delete(
    id="01FCNDV6P870EA6S7TK1DSYDG0",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — Unique identifier of the severity
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Status Pages V1
<details><summary><code>client.status_pages_v1.<a href="src/fern/status_pages_v1/client.py">listresponseincidents</a>(...) -&gt; AsyncHttpResponse[StatusPagesListResponseIncidentsResultV1]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List the linked Response incidents for a status page incident.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.status_pages_v1.listresponseincidents(
    id="abc123",
    incident_id="abc123",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — ID of the status page
    
</dd>
</dl>

<dl>
<dd>

**incident_id:** `str` — ID of the status page incident
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Actions V2
<details><summary><code>client.actions_v2.<a href="src/fern/actions_v2/client.py">list</a>(...) -&gt; AsyncHttpResponse[ActionsListResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List all actions for an organisation.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.actions_v2.list(
    incident_id="01FCNDV6P870EA6S7TK1DSYDG0",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**incident_id:** `typing.Optional[str]` — Find actions related to this incident
    
</dd>
</dl>

<dl>
<dd>

**incident_mode:** `typing.Optional[ActionsV2ListRequestIncidentMode]` — Filter to actions from incidents of the given mode. If not set, only actions from `standard` and `retrospective` incidents are returned
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.actions_v2.<a href="src/fern/actions_v2/client.py">show</a>(...) -&gt; AsyncHttpResponse[ActionsShowResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a single incident action.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.actions_v2.show(
    id="01FCNDV6P870EA6S7TK1DSYDG0",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — Unique identifier for the action
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Alert Attributes V2
<details><summary><code>client.alert_attributes_v2.<a href="src/fern/alert_attributes_v2/client.py">list</a>() -&gt; AsyncHttpResponse[AlertAttributesListResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List alert attributes.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.alert_attributes_v2.list()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.alert_attributes_v2.<a href="src/fern/alert_attributes_v2/client.py">create</a>(...) -&gt; AsyncHttpResponse[AlertAttributesCreateResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new alert attribute.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.alert_attributes_v2.create(
    array=False,
    name="service",
    required=False,
    type='CatalogEntry["01GW2G3V0S59R238FAHPDS1R67"]',
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**array:** `bool` — Whether this attribute is an array
    
</dd>
</dl>

<dl>
<dd>

**name:** `str` — Unique name of this attribute
    
</dd>
</dl>

<dl>
<dd>

**type:** `str` — Engine resource name for this attribute
    
</dd>
</dl>

<dl>
<dd>

**required:** `typing.Optional[bool]` — Whether this attribute is required. If this field is not set, the existing setting will be preserved.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.alert_attributes_v2.<a href="src/fern/alert_attributes_v2/client.py">show</a>(...) -&gt; AsyncHttpResponse[AlertAttributesShowResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Show an alert attribute.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.alert_attributes_v2.show(
    id="01GW2G3V0S59R238FAHPDS1R66",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — The ID of this attribute
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.alert_attributes_v2.<a href="src/fern/alert_attributes_v2/client.py">update</a>(...) -&gt; AsyncHttpResponse[AlertAttributesUpdateResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update an alert attribute.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.alert_attributes_v2.update(
    id="01GW2G3V0S59R238FAHPDS1R66",
    array=False,
    name="service",
    required=False,
    type='CatalogEntry["01GW2G3V0S59R238FAHPDS1R67"]',
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — The ID of this attribute
    
</dd>
</dl>

<dl>
<dd>

**array:** `bool` — Whether this attribute is an array
    
</dd>
</dl>

<dl>
<dd>

**name:** `str` — Unique name of this attribute
    
</dd>
</dl>

<dl>
<dd>

**type:** `str` — Engine resource name for this attribute
    
</dd>
</dl>

<dl>
<dd>

**required:** `typing.Optional[bool]` — Whether this attribute is required. If this field is not set, the existing setting will be preserved.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.alert_attributes_v2.<a href="src/fern/alert_attributes_v2/client.py">destroy</a>(...) -&gt; AsyncHttpResponse[None]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Destroy an alert attribute.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.alert_attributes_v2.destroy(
    id="01GW2G3V0S59R238FAHPDS1R66",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — The ID of this attribute
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Alert Events V2
<details><summary><code>client.alert_events_v2.<a href="src/fern/alert_events_v2/client.py">createhttp</a>(...) -&gt; AsyncHttpResponse[AlertEventsCreateHttpResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create an alert event using an HTTP source.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.alert_events_v2.createhttp(
    alert_source_config_id="01GW2G3V0S59R238FAHPDS1R66",
    token="some-random-string",
    deduplication_key="4293868629",
    description="We've detected a number of timeouts on hello.world.com, the service may be down. To fix...",
    metadata={"service": "hello.world.com", "team": ["my-team"]},
    source_url="https://www.my-alerting-platform.com/alerts/my-alert-123",
    status="firing",
    title="*errors.withMessage: PG::Error failed to connect",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**alert_source_config_id:** `str` — Which alert source config produced this alert
    
</dd>
</dl>

<dl>
<dd>

**status:** `AlertEventsCreateHttpPayloadV2Status` — Current status of this alert
    
</dd>
</dl>

<dl>
<dd>

**title:** `str` — The title of the alert, parsed from the alert payload according to the alert source configuration
    
</dd>
</dl>

<dl>
<dd>

**token:** `typing.Optional[str]` — Token used to authenticate the request, generated when configuring the alert source. Will be consumed via a URL query string parameter
    
</dd>
</dl>

<dl>
<dd>

**deduplication_key:** `typing.Optional[str]` 

A deduplication key which uniquely references this alert from your alert source. For newly created HTTP sources, this field is required.
If you send an event with the same deduplication_key multiple times, only one alert will be created in incident.io for this alert source config.
You can filter on this field to find the alert created by an event you've sent us.
    
</dd>
</dl>

<dl>
<dd>

**description:** `typing.Optional[str]` — Description that optionally adds more detail to title. Supports markdown.
    
</dd>
</dl>

<dl>
<dd>

**metadata:** `typing.Optional[typing.Dict[str, typing.Any]]` — Any additional metadata that you've configured your alert source to parse
    
</dd>
</dl>

<dl>
<dd>

**source_url:** `typing.Optional[str]` — If applicable, a link to the alert in the upstream system
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Alert Routes V2
<details><summary><code>client.alert_routes_v2.<a href="src/fern/alert_routes_v2/client.py">list</a>(...) -&gt; AsyncHttpResponse[AlertRoutesListResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List all alert routes in your account.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.alert_routes_v2.list(
    page_size=25,
    after="01FCNDV6P870EA6S7TK1DSYDG0",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**page_size:** `int` — Number of alert routes to return per page
    
</dd>
</dl>

<dl>
<dd>

**after:** `typing.Optional[str]` — The ID of the last alert route on the previous page
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.alert_routes_v2.<a href="src/fern/alert_routes_v2/client.py">create</a>(...) -&gt; AsyncHttpResponse[AlertRoutesCreateResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new alert route in your account.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
import datetime

from fern import (
    AlertRouteAlertSourcePayloadV2,
    AlertRouteAutoGeneratedTemplateBindingPayloadV2,
    AlertRouteChannelConfigPayloadV2,
    AlertRouteChannelTargetPayloadV2,
    AlertRouteCustomFieldBindingPayloadV2,
    AlertRouteEscalationConfigPayloadV2,
    AlertRouteEscalationTargetPayloadV2,
    AlertRouteIncidentConfigPayloadV2,
    AlertRouteIncidentTemplatePayloadV2,
    AlertRouteSeverityBindingPayloadV2,
    AlertRouteTemplateBindingPayloadV2,
    ConditionGroupPayloadV2,
    ConditionPayloadV2,
    EngineParamBindingPayloadV2,
    EngineParamBindingValuePayloadV2,
    ExpressionBranchesOptsPayloadV2,
    ExpressionBranchPayloadV2,
    ExpressionConcatenateOptsPayloadV2,
    ExpressionElseBranchPayloadV2,
    ExpressionFilterOptsPayloadV2,
    ExpressionNavigateOptsPayloadV2,
    ExpressionOperationPayloadV2,
    ExpressionParseOptsPayloadV2,
    ExpressionPayloadV2,
    GroupingKeyV2,
    IncidentIO,
    ReturnsMetaV2,
)

client = IncidentIO()
client.alert_routes_v2.create(
    alert_sources=[
        AlertRouteAlertSourcePayloadV2(
            alert_source_id="01FCNDV6P870EA6S7TK1DSYDG0",
            condition_groups=[
                ConditionGroupPayloadV2(
                    conditions=[
                        ConditionPayloadV2(
                            operation="one_of",
                            param_bindings=[
                                EngineParamBindingPayloadV2(
                                    array_value=[
                                        EngineParamBindingValuePayloadV2(
                                            literal="SEV123",
                                            reference="incident.severity",
                                        )
                                    ],
                                    value=EngineParamBindingValuePayloadV2(
                                        literal="SEV123",
                                        reference="incident.severity",
                                    ),
                                )
                            ],
                            subject="incident.severity",
                        )
                    ],
                )
            ],
        )
    ],
    channel_config=[
        AlertRouteChannelConfigPayloadV2(
            condition_groups=[
                ConditionGroupPayloadV2(
                    conditions=[
                        ConditionPayloadV2(
                            operation="one_of",
                            param_bindings=[
                                EngineParamBindingPayloadV2(
                                    array_value=[
                                        EngineParamBindingValuePayloadV2(
                                            literal="SEV123",
                                            reference="incident.severity",
                                        )
                                    ],
                                    value=EngineParamBindingValuePayloadV2(
                                        literal="SEV123",
                                        reference="incident.severity",
                                    ),
                                )
                            ],
                            subject="incident.severity",
                        )
                    ],
                )
            ],
            ms_teams_targets=AlertRouteChannelTargetPayloadV2(
                binding=EngineParamBindingPayloadV2(
                    array_value=[
                        EngineParamBindingValuePayloadV2(
                            literal="SEV123",
                            reference="incident.severity",
                        )
                    ],
                    value=EngineParamBindingValuePayloadV2(
                        literal="SEV123",
                        reference="incident.severity",
                    ),
                ),
                channel_visibility="abc123",
            ),
            slack_targets=AlertRouteChannelTargetPayloadV2(
                binding=EngineParamBindingPayloadV2(
                    array_value=[
                        EngineParamBindingValuePayloadV2(
                            literal="SEV123",
                            reference="incident.severity",
                        )
                    ],
                    value=EngineParamBindingValuePayloadV2(
                        literal="SEV123",
                        reference="incident.severity",
                    ),
                ),
                channel_visibility="abc123",
            ),
        )
    ],
    condition_groups=[
        ConditionGroupPayloadV2(
            conditions=[
                ConditionPayloadV2(
                    operation="one_of",
                    param_bindings=[
                        EngineParamBindingPayloadV2(
                            array_value=[
                                EngineParamBindingValuePayloadV2(
                                    literal="SEV123",
                                    reference="incident.severity",
                                )
                            ],
                            value=EngineParamBindingValuePayloadV2(
                                literal="SEV123",
                                reference="incident.severity",
                            ),
                        )
                    ],
                    subject="incident.severity",
                )
            ],
        )
    ],
    created_at=datetime.datetime.fromisoformat(
        "2021-08-17 13:28:57+00:00",
    ),
    enabled=False,
    escalation_config=AlertRouteEscalationConfigPayloadV2(
        auto_cancel_escalations=False,
        escalation_targets=[
            AlertRouteEscalationTargetPayloadV2(
                escalation_paths=EngineParamBindingPayloadV2(
                    array_value=[
                        EngineParamBindingValuePayloadV2(
                            literal="SEV123",
                            reference="incident.severity",
                        )
                    ],
                    value=EngineParamBindingValuePayloadV2(
                        literal="SEV123",
                        reference="incident.severity",
                    ),
                ),
                users=EngineParamBindingPayloadV2(
                    array_value=[
                        EngineParamBindingValuePayloadV2(
                            literal="SEV123",
                            reference="incident.severity",
                        )
                    ],
                    value=EngineParamBindingValuePayloadV2(
                        literal="SEV123",
                        reference="incident.severity",
                    ),
                ),
            )
        ],
    ),
    expressions=[
        ExpressionPayloadV2(
            else_branch=ExpressionElseBranchPayloadV2(
                result=EngineParamBindingPayloadV2(
                    array_value=[
                        EngineParamBindingValuePayloadV2(
                            literal="SEV123",
                            reference="incident.severity",
                        )
                    ],
                    value=EngineParamBindingValuePayloadV2(
                        literal="SEV123",
                        reference="incident.severity",
                    ),
                ),
            ),
            label="Team Slack channel",
            operations=[
                ExpressionOperationPayloadV2(
                    branches=ExpressionBranchesOptsPayloadV2(
                        branches=[
                            ExpressionBranchPayloadV2(
                                condition_groups=[
                                    ConditionGroupPayloadV2(
                                        conditions=[
                                            ConditionPayloadV2(
                                                operation="one_of",
                                                param_bindings=[
                                                    EngineParamBindingPayloadV2(
                                                        array_value=[
                                                            EngineParamBindingValuePayloadV2(
                                                                literal="SEV123",
                                                                reference="incident.severity",
                                                            )
                                                        ],
                                                        value=EngineParamBindingValuePayloadV2(
                                                            literal="SEV123",
                                                            reference="incident.severity",
                                                        ),
                                                    )
                                                ],
                                                subject="incident.severity",
                                            )
                                        ],
                                    )
                                ],
                                result=EngineParamBindingPayloadV2(
                                    array_value=[
                                        EngineParamBindingValuePayloadV2(
                                            literal="SEV123",
                                            reference="incident.severity",
                                        )
                                    ],
                                    value=EngineParamBindingValuePayloadV2(
                                        literal="SEV123",
                                        reference="incident.severity",
                                    ),
                                ),
                            )
                        ],
                        returns=ReturnsMetaV2(
                            array=True,
                            type="IncidentStatus",
                        ),
                    ),
                    concatenate=ExpressionConcatenateOptsPayloadV2(
                        reference='catalog_attribute["01FCNDV6P870EA6S7TK1DSYD5H"]',
                    ),
                    filter=ExpressionFilterOptsPayloadV2(
                        condition_groups=[
                            ConditionGroupPayloadV2(
                                conditions=[
                                    ConditionPayloadV2(
                                        operation="one_of",
                                        param_bindings=[
                                            EngineParamBindingPayloadV2(
                                                array_value=[
                                                    EngineParamBindingValuePayloadV2(
                                                        literal="SEV123",
                                                        reference="incident.severity",
                                                    )
                                                ],
                                                value=EngineParamBindingValuePayloadV2(
                                                    literal="SEV123",
                                                    reference="incident.severity",
                                                ),
                                            )
                                        ],
                                        subject="incident.severity",
                                    )
                                ],
                            )
                        ],
                    ),
                    navigate=ExpressionNavigateOptsPayloadV2(
                        reference='catalog_attribute["01FCNDV6P870EA6S7TK1DSYD5H"]',
                    ),
                    operation_type="navigate",
                    parse=ExpressionParseOptsPayloadV2(
                        returns=ReturnsMetaV2(
                            array=True,
                            type="IncidentStatus",
                        ),
                        source='metadata.annotations["github.com/repo"]',
                    ),
                )
            ],
            reference="abc123",
            root_reference="incident.status",
        )
    ],
    incident_config=AlertRouteIncidentConfigPayloadV2(
        auto_decline_enabled=False,
        auto_relate_grouped_alerts=False,
        condition_groups=[
            ConditionGroupPayloadV2(
                conditions=[
                    ConditionPayloadV2(
                        operation="one_of",
                        param_bindings=[
                            EngineParamBindingPayloadV2(
                                array_value=[
                                    EngineParamBindingValuePayloadV2(
                                        literal="SEV123",
                                        reference="incident.severity",
                                    )
                                ],
                                value=EngineParamBindingValuePayloadV2(
                                    literal="SEV123",
                                    reference="incident.severity",
                                ),
                            )
                        ],
                        subject="incident.severity",
                    )
                ],
            )
        ],
        defer_time_seconds=1,
        enabled=False,
        grouping_keys=[
            GroupingKeyV2(
                reference="alert.title",
            )
        ],
        grouping_window_seconds=1,
    ),
    incident_template=AlertRouteIncidentTemplatePayloadV2(
        custom_fields=[
            AlertRouteCustomFieldBindingPayloadV2(
                binding=EngineParamBindingPayloadV2(
                    array_value=[
                        EngineParamBindingValuePayloadV2(
                            literal="SEV123",
                            reference="incident.severity",
                        )
                    ],
                    value=EngineParamBindingValuePayloadV2(
                        literal="SEV123",
                        reference="incident.severity",
                    ),
                ),
                custom_field_id="01FCNDV6P870EA6S7TK1DSYDG0",
                merge_strategy="first-wins",
            )
        ],
        incident_mode=AlertRouteTemplateBindingPayloadV2(
            binding=EngineParamBindingPayloadV2(
                array_value=[
                    EngineParamBindingValuePayloadV2(
                        literal="SEV123",
                        reference="incident.severity",
                    )
                ],
                value=EngineParamBindingValuePayloadV2(
                    literal="SEV123",
                    reference="incident.severity",
                ),
            ),
        ),
        incident_type=AlertRouteTemplateBindingPayloadV2(
            binding=EngineParamBindingPayloadV2(
                array_value=[
                    EngineParamBindingValuePayloadV2(
                        literal="SEV123",
                        reference="incident.severity",
                    )
                ],
                value=EngineParamBindingValuePayloadV2(
                    literal="SEV123",
                    reference="incident.severity",
                ),
            ),
        ),
        name=AlertRouteAutoGeneratedTemplateBindingPayloadV2(
            autogenerated=False,
            binding=EngineParamBindingPayloadV2(
                array_value=[
                    EngineParamBindingValuePayloadV2(
                        literal="SEV123",
                        reference="incident.severity",
                    )
                ],
                value=EngineParamBindingValuePayloadV2(
                    literal="SEV123",
                    reference="incident.severity",
                ),
            ),
        ),
        severity=AlertRouteSeverityBindingPayloadV2(
            binding=EngineParamBindingPayloadV2(
                array_value=[
                    EngineParamBindingValuePayloadV2(
                        literal="SEV123",
                        reference="incident.severity",
                    )
                ],
                value=EngineParamBindingValuePayloadV2(
                    literal="SEV123",
                    reference="incident.severity",
                ),
            ),
            merge_strategy="first-wins",
        ),
        start_in_triage=AlertRouteTemplateBindingPayloadV2(
            binding=EngineParamBindingPayloadV2(
                array_value=[
                    EngineParamBindingValuePayloadV2(
                        literal="SEV123",
                        reference="incident.severity",
                    )
                ],
                value=EngineParamBindingValuePayloadV2(
                    literal="SEV123",
                    reference="incident.severity",
                ),
            ),
        ),
        summary=AlertRouteAutoGeneratedTemplateBindingPayloadV2(
            autogenerated=False,
            binding=EngineParamBindingPayloadV2(
                array_value=[
                    EngineParamBindingValuePayloadV2(
                        literal="SEV123",
                        reference="incident.severity",
                    )
                ],
                value=EngineParamBindingValuePayloadV2(
                    literal="SEV123",
                    reference="incident.severity",
                ),
            ),
        ),
        workspace=AlertRouteTemplateBindingPayloadV2(
            binding=EngineParamBindingPayloadV2(
                array_value=[
                    EngineParamBindingValuePayloadV2(
                        literal="SEV123",
                        reference="incident.severity",
                    )
                ],
                value=EngineParamBindingValuePayloadV2(
                    literal="SEV123",
                    reference="incident.severity",
                ),
            ),
        ),
    ),
    is_private=False,
    name="Production incidents",
    owning_team_ids=["01G0J1EXE7AXZ2C93K61WBPYEH"],
    updated_at=datetime.datetime.fromisoformat(
        "2021-08-17 13:28:57+00:00",
    ),
    version=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**alert_sources:** `typing.Sequence[AlertRouteAlertSourcePayloadV2]` — Which alert sources should this alert route match?
    
</dd>
</dl>

<dl>
<dd>

**channel_config:** `typing.Sequence[AlertRouteChannelConfigPayloadV2]` — The channel configuration for this alert route
    
</dd>
</dl>

<dl>
<dd>

**condition_groups:** `typing.Sequence[ConditionGroupPayloadV2]` — What condition groups must be true for this alert route to fire?
    
</dd>
</dl>

<dl>
<dd>

**enabled:** `bool` — Whether this alert route is enabled or not
    
</dd>
</dl>

<dl>
<dd>

**escalation_config:** `AlertRouteEscalationConfigPayloadV2` 
    
</dd>
</dl>

<dl>
<dd>

**expressions:** `typing.Sequence[ExpressionPayloadV2]` — The expressions used in this template
    
</dd>
</dl>

<dl>
<dd>

**incident_config:** `AlertRouteIncidentConfigPayloadV2` 
    
</dd>
</dl>

<dl>
<dd>

**incident_template:** `AlertRouteIncidentTemplatePayloadV2` 
    
</dd>
</dl>

<dl>
<dd>

**is_private:** `bool` — Whether this alert route is private. Private alert routes will only create private incidents from alerts.
    
</dd>
</dl>

<dl>
<dd>

**name:** `str` — The name of this alert route config, for the user's reference
    
</dd>
</dl>

<dl>
<dd>

**version:** `int` — The version of this alert route config
    
</dd>
</dl>

<dl>
<dd>

**created_at:** `typing.Optional[dt.datetime]` — The time of creation of this alert route
    
</dd>
</dl>

<dl>
<dd>

**owning_team_ids:** `typing.Optional[typing.Sequence[str]]` — IDs of teams that own this alert route
    
</dd>
</dl>

<dl>
<dd>

**updated_at:** `typing.Optional[dt.datetime]` — The time of last update of this alert route
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.alert_routes_v2.<a href="src/fern/alert_routes_v2/client.py">show</a>(...) -&gt; AsyncHttpResponse[AlertRoutesShowResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Load details about a specific alert route in your account.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.alert_routes_v2.show(
    id="01FCNDV6P870EA6S7TK1DSYDG0",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — Unique identifier of the alert route
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.alert_routes_v2.<a href="src/fern/alert_routes_v2/client.py">update</a>(...) -&gt; AsyncHttpResponse[AlertRoutesUpdateResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update an existing alert route in your account.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
import datetime

from fern import (
    AlertRouteAlertSourcePayloadV2,
    AlertRouteAutoGeneratedTemplateBindingPayloadV2,
    AlertRouteChannelConfigPayloadV2,
    AlertRouteChannelTargetPayloadV2,
    AlertRouteCustomFieldBindingPayloadV2,
    AlertRouteEscalationConfigPayloadV2,
    AlertRouteEscalationTargetPayloadV2,
    AlertRouteIncidentConfigPayloadV2,
    AlertRouteIncidentTemplatePayloadV2,
    AlertRouteSeverityBindingPayloadV2,
    AlertRouteTemplateBindingPayloadV2,
    ConditionGroupPayloadV2,
    ConditionPayloadV2,
    EngineParamBindingPayloadV2,
    EngineParamBindingValuePayloadV2,
    ExpressionBranchesOptsPayloadV2,
    ExpressionBranchPayloadV2,
    ExpressionConcatenateOptsPayloadV2,
    ExpressionElseBranchPayloadV2,
    ExpressionFilterOptsPayloadV2,
    ExpressionNavigateOptsPayloadV2,
    ExpressionOperationPayloadV2,
    ExpressionParseOptsPayloadV2,
    ExpressionPayloadV2,
    GroupingKeyV2,
    IncidentIO,
    ReturnsMetaV2,
)

client = IncidentIO()
client.alert_routes_v2.update(
    id="01FCNDV6P870EA6S7TK1DSYDG0",
    alert_sources=[
        AlertRouteAlertSourcePayloadV2(
            alert_source_id="01FCNDV6P870EA6S7TK1DSYDG0",
            condition_groups=[
                ConditionGroupPayloadV2(
                    conditions=[
                        ConditionPayloadV2(
                            operation="one_of",
                            param_bindings=[
                                EngineParamBindingPayloadV2(
                                    array_value=[
                                        EngineParamBindingValuePayloadV2(
                                            literal="SEV123",
                                            reference="incident.severity",
                                        )
                                    ],
                                    value=EngineParamBindingValuePayloadV2(
                                        literal="SEV123",
                                        reference="incident.severity",
                                    ),
                                )
                            ],
                            subject="incident.severity",
                        )
                    ],
                )
            ],
        )
    ],
    channel_config=[
        AlertRouteChannelConfigPayloadV2(
            condition_groups=[
                ConditionGroupPayloadV2(
                    conditions=[
                        ConditionPayloadV2(
                            operation="one_of",
                            param_bindings=[
                                EngineParamBindingPayloadV2(
                                    array_value=[
                                        EngineParamBindingValuePayloadV2(
                                            literal="SEV123",
                                            reference="incident.severity",
                                        )
                                    ],
                                    value=EngineParamBindingValuePayloadV2(
                                        literal="SEV123",
                                        reference="incident.severity",
                                    ),
                                )
                            ],
                            subject="incident.severity",
                        )
                    ],
                )
            ],
            ms_teams_targets=AlertRouteChannelTargetPayloadV2(
                binding=EngineParamBindingPayloadV2(
                    array_value=[
                        EngineParamBindingValuePayloadV2(
                            literal="SEV123",
                            reference="incident.severity",
                        )
                    ],
                    value=EngineParamBindingValuePayloadV2(
                        literal="SEV123",
                        reference="incident.severity",
                    ),
                ),
                channel_visibility="abc123",
            ),
            slack_targets=AlertRouteChannelTargetPayloadV2(
                binding=EngineParamBindingPayloadV2(
                    array_value=[
                        EngineParamBindingValuePayloadV2(
                            literal="SEV123",
                            reference="incident.severity",
                        )
                    ],
                    value=EngineParamBindingValuePayloadV2(
                        literal="SEV123",
                        reference="incident.severity",
                    ),
                ),
                channel_visibility="abc123",
            ),
        )
    ],
    condition_groups=[
        ConditionGroupPayloadV2(
            conditions=[
                ConditionPayloadV2(
                    operation="one_of",
                    param_bindings=[
                        EngineParamBindingPayloadV2(
                            array_value=[
                                EngineParamBindingValuePayloadV2(
                                    literal="SEV123",
                                    reference="incident.severity",
                                )
                            ],
                            value=EngineParamBindingValuePayloadV2(
                                literal="SEV123",
                                reference="incident.severity",
                            ),
                        )
                    ],
                    subject="incident.severity",
                )
            ],
        )
    ],
    created_at=datetime.datetime.fromisoformat(
        "2021-08-17 13:28:57+00:00",
    ),
    enabled=False,
    escalation_config=AlertRouteEscalationConfigPayloadV2(
        auto_cancel_escalations=False,
        escalation_targets=[
            AlertRouteEscalationTargetPayloadV2(
                escalation_paths=EngineParamBindingPayloadV2(
                    array_value=[
                        EngineParamBindingValuePayloadV2(
                            literal="SEV123",
                            reference="incident.severity",
                        )
                    ],
                    value=EngineParamBindingValuePayloadV2(
                        literal="SEV123",
                        reference="incident.severity",
                    ),
                ),
                users=EngineParamBindingPayloadV2(
                    array_value=[
                        EngineParamBindingValuePayloadV2(
                            literal="SEV123",
                            reference="incident.severity",
                        )
                    ],
                    value=EngineParamBindingValuePayloadV2(
                        literal="SEV123",
                        reference="incident.severity",
                    ),
                ),
            )
        ],
    ),
    expressions=[
        ExpressionPayloadV2(
            else_branch=ExpressionElseBranchPayloadV2(
                result=EngineParamBindingPayloadV2(
                    array_value=[
                        EngineParamBindingValuePayloadV2(
                            literal="SEV123",
                            reference="incident.severity",
                        )
                    ],
                    value=EngineParamBindingValuePayloadV2(
                        literal="SEV123",
                        reference="incident.severity",
                    ),
                ),
            ),
            label="Team Slack channel",
            operations=[
                ExpressionOperationPayloadV2(
                    branches=ExpressionBranchesOptsPayloadV2(
                        branches=[
                            ExpressionBranchPayloadV2(
                                condition_groups=[
                                    ConditionGroupPayloadV2(
                                        conditions=[
                                            ConditionPayloadV2(
                                                operation="one_of",
                                                param_bindings=[
                                                    EngineParamBindingPayloadV2(
                                                        array_value=[
                                                            EngineParamBindingValuePayloadV2(
                                                                literal="SEV123",
                                                                reference="incident.severity",
                                                            )
                                                        ],
                                                        value=EngineParamBindingValuePayloadV2(
                                                            literal="SEV123",
                                                            reference="incident.severity",
                                                        ),
                                                    )
                                                ],
                                                subject="incident.severity",
                                            )
                                        ],
                                    )
                                ],
                                result=EngineParamBindingPayloadV2(
                                    array_value=[
                                        EngineParamBindingValuePayloadV2(
                                            literal="SEV123",
                                            reference="incident.severity",
                                        )
                                    ],
                                    value=EngineParamBindingValuePayloadV2(
                                        literal="SEV123",
                                        reference="incident.severity",
                                    ),
                                ),
                            )
                        ],
                        returns=ReturnsMetaV2(
                            array=True,
                            type="IncidentStatus",
                        ),
                    ),
                    concatenate=ExpressionConcatenateOptsPayloadV2(
                        reference='catalog_attribute["01FCNDV6P870EA6S7TK1DSYD5H"]',
                    ),
                    filter=ExpressionFilterOptsPayloadV2(
                        condition_groups=[
                            ConditionGroupPayloadV2(
                                conditions=[
                                    ConditionPayloadV2(
                                        operation="one_of",
                                        param_bindings=[
                                            EngineParamBindingPayloadV2(
                                                array_value=[
                                                    EngineParamBindingValuePayloadV2(
                                                        literal="SEV123",
                                                        reference="incident.severity",
                                                    )
                                                ],
                                                value=EngineParamBindingValuePayloadV2(
                                                    literal="SEV123",
                                                    reference="incident.severity",
                                                ),
                                            )
                                        ],
                                        subject="incident.severity",
                                    )
                                ],
                            )
                        ],
                    ),
                    navigate=ExpressionNavigateOptsPayloadV2(
                        reference='catalog_attribute["01FCNDV6P870EA6S7TK1DSYD5H"]',
                    ),
                    operation_type="navigate",
                    parse=ExpressionParseOptsPayloadV2(
                        returns=ReturnsMetaV2(
                            array=True,
                            type="IncidentStatus",
                        ),
                        source='metadata.annotations["github.com/repo"]',
                    ),
                )
            ],
            reference="abc123",
            root_reference="incident.status",
        )
    ],
    incident_config=AlertRouteIncidentConfigPayloadV2(
        auto_decline_enabled=False,
        auto_relate_grouped_alerts=False,
        condition_groups=[
            ConditionGroupPayloadV2(
                conditions=[
                    ConditionPayloadV2(
                        operation="one_of",
                        param_bindings=[
                            EngineParamBindingPayloadV2(
                                array_value=[
                                    EngineParamBindingValuePayloadV2(
                                        literal="SEV123",
                                        reference="incident.severity",
                                    )
                                ],
                                value=EngineParamBindingValuePayloadV2(
                                    literal="SEV123",
                                    reference="incident.severity",
                                ),
                            )
                        ],
                        subject="incident.severity",
                    )
                ],
            )
        ],
        defer_time_seconds=1,
        enabled=False,
        grouping_keys=[
            GroupingKeyV2(
                reference="alert.title",
            )
        ],
        grouping_window_seconds=1,
    ),
    incident_template=AlertRouteIncidentTemplatePayloadV2(
        custom_fields=[
            AlertRouteCustomFieldBindingPayloadV2(
                binding=EngineParamBindingPayloadV2(
                    array_value=[
                        EngineParamBindingValuePayloadV2(
                            literal="SEV123",
                            reference="incident.severity",
                        )
                    ],
                    value=EngineParamBindingValuePayloadV2(
                        literal="SEV123",
                        reference="incident.severity",
                    ),
                ),
                custom_field_id="01FCNDV6P870EA6S7TK1DSYDG0",
                merge_strategy="first-wins",
            )
        ],
        incident_mode=AlertRouteTemplateBindingPayloadV2(
            binding=EngineParamBindingPayloadV2(
                array_value=[
                    EngineParamBindingValuePayloadV2(
                        literal="SEV123",
                        reference="incident.severity",
                    )
                ],
                value=EngineParamBindingValuePayloadV2(
                    literal="SEV123",
                    reference="incident.severity",
                ),
            ),
        ),
        incident_type=AlertRouteTemplateBindingPayloadV2(
            binding=EngineParamBindingPayloadV2(
                array_value=[
                    EngineParamBindingValuePayloadV2(
                        literal="SEV123",
                        reference="incident.severity",
                    )
                ],
                value=EngineParamBindingValuePayloadV2(
                    literal="SEV123",
                    reference="incident.severity",
                ),
            ),
        ),
        name=AlertRouteAutoGeneratedTemplateBindingPayloadV2(
            autogenerated=False,
            binding=EngineParamBindingPayloadV2(
                array_value=[
                    EngineParamBindingValuePayloadV2(
                        literal="SEV123",
                        reference="incident.severity",
                    )
                ],
                value=EngineParamBindingValuePayloadV2(
                    literal="SEV123",
                    reference="incident.severity",
                ),
            ),
        ),
        severity=AlertRouteSeverityBindingPayloadV2(
            binding=EngineParamBindingPayloadV2(
                array_value=[
                    EngineParamBindingValuePayloadV2(
                        literal="SEV123",
                        reference="incident.severity",
                    )
                ],
                value=EngineParamBindingValuePayloadV2(
                    literal="SEV123",
                    reference="incident.severity",
                ),
            ),
            merge_strategy="first-wins",
        ),
        start_in_triage=AlertRouteTemplateBindingPayloadV2(
            binding=EngineParamBindingPayloadV2(
                array_value=[
                    EngineParamBindingValuePayloadV2(
                        literal="SEV123",
                        reference="incident.severity",
                    )
                ],
                value=EngineParamBindingValuePayloadV2(
                    literal="SEV123",
                    reference="incident.severity",
                ),
            ),
        ),
        summary=AlertRouteAutoGeneratedTemplateBindingPayloadV2(
            autogenerated=False,
            binding=EngineParamBindingPayloadV2(
                array_value=[
                    EngineParamBindingValuePayloadV2(
                        literal="SEV123",
                        reference="incident.severity",
                    )
                ],
                value=EngineParamBindingValuePayloadV2(
                    literal="SEV123",
                    reference="incident.severity",
                ),
            ),
        ),
        workspace=AlertRouteTemplateBindingPayloadV2(
            binding=EngineParamBindingPayloadV2(
                array_value=[
                    EngineParamBindingValuePayloadV2(
                        literal="SEV123",
                        reference="incident.severity",
                    )
                ],
                value=EngineParamBindingValuePayloadV2(
                    literal="SEV123",
                    reference="incident.severity",
                ),
            ),
        ),
    ),
    is_private=False,
    name="Production incidents",
    owning_team_ids=["01G0J1EXE7AXZ2C93K61WBPYEH"],
    updated_at=datetime.datetime.fromisoformat(
        "2021-08-17 13:28:57+00:00",
    ),
    version=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — Unique identifier of the alert route
    
</dd>
</dl>

<dl>
<dd>

**alert_sources:** `typing.Sequence[AlertRouteAlertSourcePayloadV2]` — Which alert sources should this alert route match?
    
</dd>
</dl>

<dl>
<dd>

**channel_config:** `typing.Sequence[AlertRouteChannelConfigPayloadV2]` — The channel configuration for this alert route
    
</dd>
</dl>

<dl>
<dd>

**condition_groups:** `typing.Sequence[ConditionGroupPayloadV2]` — What condition groups must be true for this alert route to fire?
    
</dd>
</dl>

<dl>
<dd>

**enabled:** `bool` — Whether this alert route is enabled or not
    
</dd>
</dl>

<dl>
<dd>

**escalation_config:** `AlertRouteEscalationConfigPayloadV2` 
    
</dd>
</dl>

<dl>
<dd>

**expressions:** `typing.Sequence[ExpressionPayloadV2]` — The expressions used in this template
    
</dd>
</dl>

<dl>
<dd>

**incident_config:** `AlertRouteIncidentConfigPayloadV2` 
    
</dd>
</dl>

<dl>
<dd>

**incident_template:** `AlertRouteIncidentTemplatePayloadV2` 
    
</dd>
</dl>

<dl>
<dd>

**is_private:** `bool` — Whether this alert route is private. Private alert routes will only create private incidents from alerts.
    
</dd>
</dl>

<dl>
<dd>

**name:** `str` — The name of this alert route config, for the user's reference
    
</dd>
</dl>

<dl>
<dd>

**version:** `int` — The version of this alert route config
    
</dd>
</dl>

<dl>
<dd>

**created_at:** `typing.Optional[dt.datetime]` — The time of creation of this alert route
    
</dd>
</dl>

<dl>
<dd>

**owning_team_ids:** `typing.Optional[typing.Sequence[str]]` — IDs of teams that own this alert route
    
</dd>
</dl>

<dl>
<dd>

**updated_at:** `typing.Optional[dt.datetime]` — The time of last update of this alert route
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.alert_routes_v2.<a href="src/fern/alert_routes_v2/client.py">delete</a>(...) -&gt; AsyncHttpResponse[None]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete an existing alert route in your account.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.alert_routes_v2.delete(
    id="01FCNDV6P870EA6S7TK1DSYDG0",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — Unique identifier of the alert route
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Alert Sources V2
<details><summary><code>client.alert_sources_v2.<a href="src/fern/alert_sources_v2/client.py">list</a>() -&gt; AsyncHttpResponse[AlertSourcesListResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List all alert sources in your account.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.alert_sources_v2.list()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.alert_sources_v2.<a href="src/fern/alert_sources_v2/client.py">create</a>(...) -&gt; AsyncHttpResponse[AlertSourcesCreateResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new alert source in your account.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import (
    AlertSourceHttpCustomOptionsV2,
    AlertSourceJiraOptionsV2,
    AlertTemplateAttributePayloadV2,
    AlertTemplatePayloadV2,
    ConditionGroupPayloadV2,
    ConditionPayloadV2,
    EngineParamBindingPayloadV2,
    EngineParamBindingValuePayloadV2,
    ExpressionBranchesOptsPayloadV2,
    ExpressionBranchPayloadV2,
    ExpressionConcatenateOptsPayloadV2,
    ExpressionElseBranchPayloadV2,
    ExpressionFilterOptsPayloadV2,
    ExpressionNavigateOptsPayloadV2,
    ExpressionOperationPayloadV2,
    ExpressionParseOptsPayloadV2,
    ExpressionPayloadV2,
    IncidentIO,
    ReturnsMetaV2,
)

client = IncidentIO()
client.alert_sources_v2.create(
    http_custom_options=AlertSourceHttpCustomOptionsV2(
        deduplication_key_path="$.alert_id",
        transform_expression="return {\n  title: $.title || $.name || 'Unknown Alert',\n  status: $.status === 'resolved' ? 'resolved' : 'firing',\n  description: $.description || $.message || '',\n  sourceURL: $.url || $.link || '',\n  metadata: { team: $.team, severity: $.severity }\n}",
    ),
    jira_options=AlertSourceJiraOptionsV2(
        project_ids=["01GBSQF3FHF7FWZQNWGHAVQ804", "10043"],
    ),
    name="Production Web Dashboard Alerts",
    owning_team_ids=["01G0J1EXE7AXZ2C93K61WBPYEH"],
    source_type="alertmanager",
    template=AlertTemplatePayloadV2(
        attributes=[
            AlertTemplateAttributePayloadV2(
                alert_attribute_id="abc123",
                binding=EngineParamBindingPayloadV2(
                    array_value=[
                        EngineParamBindingValuePayloadV2(
                            literal="SEV123",
                            reference="incident.severity",
                        )
                    ],
                    value=EngineParamBindingValuePayloadV2(
                        literal="SEV123",
                        reference="incident.severity",
                    ),
                ),
            )
        ],
        description=EngineParamBindingValuePayloadV2(
            literal="SEV123",
            reference="incident.severity",
        ),
        expressions=[
            ExpressionPayloadV2(
                else_branch=ExpressionElseBranchPayloadV2(
                    result=EngineParamBindingPayloadV2(
                        array_value=[
                            EngineParamBindingValuePayloadV2(
                                literal="SEV123",
                                reference="incident.severity",
                            )
                        ],
                        value=EngineParamBindingValuePayloadV2(
                            literal="SEV123",
                            reference="incident.severity",
                        ),
                    ),
                ),
                label="Team Slack channel",
                operations=[
                    ExpressionOperationPayloadV2(
                        branches=ExpressionBranchesOptsPayloadV2(
                            branches=[
                                ExpressionBranchPayloadV2(
                                    condition_groups=[
                                        ConditionGroupPayloadV2(
                                            conditions=[
                                                ConditionPayloadV2(
                                                    operation="one_of",
                                                    param_bindings=[
                                                        EngineParamBindingPayloadV2(
                                                            array_value=[
                                                                EngineParamBindingValuePayloadV2(
                                                                    literal="SEV123",
                                                                    reference="incident.severity",
                                                                )
                                                            ],
                                                            value=EngineParamBindingValuePayloadV2(
                                                                literal="SEV123",
                                                                reference="incident.severity",
                                                            ),
                                                        )
                                                    ],
                                                    subject="incident.severity",
                                                )
                                            ],
                                        )
                                    ],
                                    result=EngineParamBindingPayloadV2(
                                        array_value=[
                                            EngineParamBindingValuePayloadV2(
                                                literal="SEV123",
                                                reference="incident.severity",
                                            )
                                        ],
                                        value=EngineParamBindingValuePayloadV2(
                                            literal="SEV123",
                                            reference="incident.severity",
                                        ),
                                    ),
                                )
                            ],
                            returns=ReturnsMetaV2(
                                array=True,
                                type="IncidentStatus",
                            ),
                        ),
                        concatenate=ExpressionConcatenateOptsPayloadV2(
                            reference='catalog_attribute["01FCNDV6P870EA6S7TK1DSYD5H"]',
                        ),
                        filter=ExpressionFilterOptsPayloadV2(
                            condition_groups=[
                                ConditionGroupPayloadV2(
                                    conditions=[
                                        ConditionPayloadV2(
                                            operation="one_of",
                                            param_bindings=[
                                                EngineParamBindingPayloadV2(
                                                    array_value=[
                                                        EngineParamBindingValuePayloadV2(
                                                            literal="SEV123",
                                                            reference="incident.severity",
                                                        )
                                                    ],
                                                    value=EngineParamBindingValuePayloadV2(
                                                        literal="SEV123",
                                                        reference="incident.severity",
                                                    ),
                                                )
                                            ],
                                            subject="incident.severity",
                                        )
                                    ],
                                )
                            ],
                        ),
                        navigate=ExpressionNavigateOptsPayloadV2(
                            reference='catalog_attribute["01FCNDV6P870EA6S7TK1DSYD5H"]',
                        ),
                        operation_type="navigate",
                        parse=ExpressionParseOptsPayloadV2(
                            returns=ReturnsMetaV2(
                                array=True,
                                type="IncidentStatus",
                            ),
                            source='metadata.annotations["github.com/repo"]',
                        ),
                    )
                ],
                reference="abc123",
                root_reference="incident.status",
            )
        ],
        is_private=False,
        title=EngineParamBindingValuePayloadV2(
            literal="SEV123",
            reference="incident.severity",
        ),
        visible_to_teams=EngineParamBindingPayloadV2(
            array_value=[
                EngineParamBindingValuePayloadV2(
                    literal="SEV123",
                    reference="incident.severity",
                )
            ],
            value=EngineParamBindingValuePayloadV2(
                literal="SEV123",
                reference="incident.severity",
            ),
        ),
    ),
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**name:** `str` — Unique name of the alert source
    
</dd>
</dl>

<dl>
<dd>

**source_type:** `AlertSourcesCreatePayloadV2SourceType` — Type of alert source
    
</dd>
</dl>

<dl>
<dd>

**template:** `AlertTemplatePayloadV2` 
    
</dd>
</dl>

<dl>
<dd>

**http_custom_options:** `typing.Optional[AlertSourceHttpCustomOptionsV2]` 
    
</dd>
</dl>

<dl>
<dd>

**jira_options:** `typing.Optional[AlertSourceJiraOptionsV2]` 
    
</dd>
</dl>

<dl>
<dd>

**owning_team_ids:** `typing.Optional[typing.Sequence[str]]` — IDs of teams that own this alert source
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.alert_sources_v2.<a href="src/fern/alert_sources_v2/client.py">show</a>(...) -&gt; AsyncHttpResponse[AlertSourcesShowResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Load details about a specific alert source in your account.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.alert_sources_v2.show(
    id="01GW2G3V0S59R238FAHPDS1R66",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — The ID of this alert source
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.alert_sources_v2.<a href="src/fern/alert_sources_v2/client.py">update</a>(...) -&gt; AsyncHttpResponse[AlertSourcesUpdateResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update an existing alert source in your account.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import (
    AlertSourceHttpCustomOptionsV2,
    AlertSourceJiraOptionsV2,
    AlertTemplateAttributePayloadV2,
    AlertTemplatePayloadV2,
    ConditionGroupPayloadV2,
    ConditionPayloadV2,
    EngineParamBindingPayloadV2,
    EngineParamBindingValuePayloadV2,
    ExpressionBranchesOptsPayloadV2,
    ExpressionBranchPayloadV2,
    ExpressionConcatenateOptsPayloadV2,
    ExpressionElseBranchPayloadV2,
    ExpressionFilterOptsPayloadV2,
    ExpressionNavigateOptsPayloadV2,
    ExpressionOperationPayloadV2,
    ExpressionParseOptsPayloadV2,
    ExpressionPayloadV2,
    IncidentIO,
    ReturnsMetaV2,
)

client = IncidentIO()
client.alert_sources_v2.update(
    id="01GW2G3V0S59R238FAHPDS1R66",
    http_custom_options=AlertSourceHttpCustomOptionsV2(
        deduplication_key_path="$.alert_id",
        transform_expression="return {\n  title: $.title || $.name || 'Unknown Alert',\n  status: $.status === 'resolved' ? 'resolved' : 'firing',\n  description: $.description || $.message || '',\n  sourceURL: $.url || $.link || '',\n  metadata: { team: $.team, severity: $.severity }\n}",
    ),
    jira_options=AlertSourceJiraOptionsV2(
        project_ids=["01GBSQF3FHF7FWZQNWGHAVQ804", "10043"],
    ),
    name="Production Web Dashboard Alerts",
    owning_team_ids=["01G0J1EXE7AXZ2C93K61WBPYEH"],
    template=AlertTemplatePayloadV2(
        attributes=[
            AlertTemplateAttributePayloadV2(
                alert_attribute_id="abc123",
                binding=EngineParamBindingPayloadV2(
                    array_value=[
                        EngineParamBindingValuePayloadV2(
                            literal="SEV123",
                            reference="incident.severity",
                        )
                    ],
                    value=EngineParamBindingValuePayloadV2(
                        literal="SEV123",
                        reference="incident.severity",
                    ),
                ),
            )
        ],
        description=EngineParamBindingValuePayloadV2(
            literal="SEV123",
            reference="incident.severity",
        ),
        expressions=[
            ExpressionPayloadV2(
                else_branch=ExpressionElseBranchPayloadV2(
                    result=EngineParamBindingPayloadV2(
                        array_value=[
                            EngineParamBindingValuePayloadV2(
                                literal="SEV123",
                                reference="incident.severity",
                            )
                        ],
                        value=EngineParamBindingValuePayloadV2(
                            literal="SEV123",
                            reference="incident.severity",
                        ),
                    ),
                ),
                label="Team Slack channel",
                operations=[
                    ExpressionOperationPayloadV2(
                        branches=ExpressionBranchesOptsPayloadV2(
                            branches=[
                                ExpressionBranchPayloadV2(
                                    condition_groups=[
                                        ConditionGroupPayloadV2(
                                            conditions=[
                                                ConditionPayloadV2(
                                                    operation="one_of",
                                                    param_bindings=[
                                                        EngineParamBindingPayloadV2(
                                                            array_value=[
                                                                EngineParamBindingValuePayloadV2(
                                                                    literal="SEV123",
                                                                    reference="incident.severity",
                                                                )
                                                            ],
                                                            value=EngineParamBindingValuePayloadV2(
                                                                literal="SEV123",
                                                                reference="incident.severity",
                                                            ),
                                                        )
                                                    ],
                                                    subject="incident.severity",
                                                )
                                            ],
                                        )
                                    ],
                                    result=EngineParamBindingPayloadV2(
                                        array_value=[
                                            EngineParamBindingValuePayloadV2(
                                                literal="SEV123",
                                                reference="incident.severity",
                                            )
                                        ],
                                        value=EngineParamBindingValuePayloadV2(
                                            literal="SEV123",
                                            reference="incident.severity",
                                        ),
                                    ),
                                )
                            ],
                            returns=ReturnsMetaV2(
                                array=True,
                                type="IncidentStatus",
                            ),
                        ),
                        concatenate=ExpressionConcatenateOptsPayloadV2(
                            reference='catalog_attribute["01FCNDV6P870EA6S7TK1DSYD5H"]',
                        ),
                        filter=ExpressionFilterOptsPayloadV2(
                            condition_groups=[
                                ConditionGroupPayloadV2(
                                    conditions=[
                                        ConditionPayloadV2(
                                            operation="one_of",
                                            param_bindings=[
                                                EngineParamBindingPayloadV2(
                                                    array_value=[
                                                        EngineParamBindingValuePayloadV2(
                                                            literal="SEV123",
                                                            reference="incident.severity",
                                                        )
                                                    ],
                                                    value=EngineParamBindingValuePayloadV2(
                                                        literal="SEV123",
                                                        reference="incident.severity",
                                                    ),
                                                )
                                            ],
                                            subject="incident.severity",
                                        )
                                    ],
                                )
                            ],
                        ),
                        navigate=ExpressionNavigateOptsPayloadV2(
                            reference='catalog_attribute["01FCNDV6P870EA6S7TK1DSYD5H"]',
                        ),
                        operation_type="navigate",
                        parse=ExpressionParseOptsPayloadV2(
                            returns=ReturnsMetaV2(
                                array=True,
                                type="IncidentStatus",
                            ),
                            source='metadata.annotations["github.com/repo"]',
                        ),
                    )
                ],
                reference="abc123",
                root_reference="incident.status",
            )
        ],
        is_private=False,
        title=EngineParamBindingValuePayloadV2(
            literal="SEV123",
            reference="incident.severity",
        ),
        visible_to_teams=EngineParamBindingPayloadV2(
            array_value=[
                EngineParamBindingValuePayloadV2(
                    literal="SEV123",
                    reference="incident.severity",
                )
            ],
            value=EngineParamBindingValuePayloadV2(
                literal="SEV123",
                reference="incident.severity",
            ),
        ),
    ),
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — The ID of this alert source
    
</dd>
</dl>

<dl>
<dd>

**name:** `str` — Unique name of the alert source
    
</dd>
</dl>

<dl>
<dd>

**template:** `AlertTemplatePayloadV2` 
    
</dd>
</dl>

<dl>
<dd>

**http_custom_options:** `typing.Optional[AlertSourceHttpCustomOptionsV2]` 
    
</dd>
</dl>

<dl>
<dd>

**jira_options:** `typing.Optional[AlertSourceJiraOptionsV2]` 
    
</dd>
</dl>

<dl>
<dd>

**owning_team_ids:** `typing.Optional[typing.Sequence[str]]` — IDs of teams that own this alert source
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.alert_sources_v2.<a href="src/fern/alert_sources_v2/client.py">delete</a>(...) -&gt; AsyncHttpResponse[None]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete an existing alert source in your account.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.alert_sources_v2.delete(
    id="01GW2G3V0S59R238FAHPDS1R66",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — The ID of this alert source
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Alerts V2
<details><summary><code>client.alerts_v2.<a href="src/fern/alerts_v2/client.py">list</a>(...) -&gt; AsyncHttpResponse[AlertsListResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List all alerts for your account.
		
This endpoint supports a number of filters, which can help find alerts matching certain
criteria. These filters work similarly to the filters on the incidents endpoint, where 
a field is specified alongside a comparison operator in the query string.

Note that:
- Filters may be used together, and the result will be alerts that match all filters.
- All query parameters must be URI encoded.

### By deduplication_key

Find all alerts with deduplication_key ABC:

		curl --get 'https://api.incident.io/v2/alerts' \
			--data 'deduplication_key[is]=ABC'

### By status

Find all alerts in a firing state:

		curl --get 'https://api.incident.io/v2/alerts' \
			--data 'status[one_of]=firing'

### By created_at
Find all alerts that follow specified date parameters for created_at field.
Possible values are "gte" (greater than or equal to), "lte" (less than or equal to), and 
"date_range" (between two dates). The following example finds all alerts created after 
2025-01-01:

		curl --get 'https://api.incident.io/v2/alerts' \
			--data 'created_at[gte]=2025-01-01'

To find alerts created within a specific date range, use the date_range option with 
tilde-separated dates:

		curl --get 'https://api.incident.io/v2/alerts' \
			--data 'created_at[date_range]=2024-12-02~2024-12-08'
		
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.alerts_v2.list(
    page_size=25,
    after="01FCNDV6P870EA6S7TK1DSYDG0",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**page_size:** `int` — Number of alerts to return per page
    
</dd>
</dl>

<dl>
<dd>

**after:** `typing.Optional[str]` — If provided, pass this as the 'after' param to load the next page
    
</dd>
</dl>

<dl>
<dd>

**deduplication_key:** `typing.Optional[typing.Dict[str, typing.Sequence[str]]]` — Filter on alert deduplication key. The accepted operator is 'is'.
    
</dd>
</dl>

<dl>
<dd>

**status:** `typing.Optional[typing.Dict[str, typing.Sequence[str]]]` — Filter on alert status. The accepted operators are 'one_of', or 'not_in'.
    
</dd>
</dl>

<dl>
<dd>

**created_at:** `typing.Optional[typing.Dict[str, typing.Sequence[str]]]` — Filter on alert created at timestamp. Accepted operators are 'gte', 'lte' and 'date_range'.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.alerts_v2.<a href="src/fern/alerts_v2/client.py">show</a>(...) -&gt; AsyncHttpResponse[AlertsShowResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Show a single alert for your account
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.alerts_v2.show(
    id="01FDAG4SAP5TYPT98WGR2N7W91",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — Unique identifier for the alert
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.alerts_v2.<a href="src/fern/alerts_v2/client.py">listincidentalerts</a>(...) -&gt; AsyncHttpResponse[AlertsListIncidentAlertsResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List the connections between incidents and alerts
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.alerts_v2.listincidentalerts(
    page_size=25,
    after="01FCNDV6P870EA6S7TK1DSYDG0",
    alert_id="01FCNDV6P870EA6S7TK1DSYDG1",
    incident_id="01FCNDV6P870EA6S7TK1DSYDG0",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**page_size:** `int` — Number of incident alerts to return per page
    
</dd>
</dl>

<dl>
<dd>

**after:** `typing.Optional[str]` — If provided, pass this as the 'after' param to load the next page
    
</dd>
</dl>

<dl>
<dd>

**alert_id:** `typing.Optional[str]` — Alert that this incident alert refers to
    
</dd>
</dl>

<dl>
<dd>

**incident_id:** `typing.Optional[str]` — Incident that this incident alert is attached to
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Catalog V2
<details><summary><code>client.catalog_v2.<a href="src/fern/catalog_v2/client.py">listentries</a>(...) -&gt; AsyncHttpResponse[CatalogListEntriesResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List entries for a catalog type.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.catalog_v2.listentries(
    catalog_type_id="01FCNDV6P870EA6S7TK1DSYDG0",
    page_size=25,
    after="01FDAG4SAP5TYPT98WGR2N7W91",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**catalog_type_id:** `str` — ID of this catalog type
    
</dd>
</dl>

<dl>
<dd>

**page_size:** `typing.Optional[int]` — Integer number of records to return
    
</dd>
</dl>

<dl>
<dd>

**after:** `typing.Optional[str]` — An record's ID. This endpoint will return a list of records after this ID in relation to the API response order.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.catalog_v2.<a href="src/fern/catalog_v2/client.py">createentry</a>(...) -&gt; AsyncHttpResponse[CatalogCreateEntryResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create an entry within the catalog. We support a maximum of 50,000 entries per type.

If you call this API with a payload where the external_id and catalog_type_id match an existing entry, the existing entry will be updated.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import (
    EngineParamBindingPayloadV2,
    EngineParamBindingValuePayloadV2,
    IncidentIO,
)

client = IncidentIO()
client.catalog_v2.createentry(
    aliases=["lawrence@incident.io", "lawrence"],
    attribute_values={
        "abc123": EngineParamBindingPayloadV2(
            array_value=[
                EngineParamBindingValuePayloadV2(
                    literal="SEV123",
                    reference="incident.severity",
                )
            ],
            value=EngineParamBindingValuePayloadV2(
                literal="SEV123",
                reference="incident.severity",
            ),
        )
    },
    catalog_type_id="01FCNDV6P870EA6S7TK1DSYDG0",
    external_id="761722cd-d1d7-477b-ac7e-90f9e079dc33",
    name="Primary On-call",
    rank=3,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**attribute_values:** `typing.Dict[str, EngineParamBindingPayloadV2]` — Values of this entry
    
</dd>
</dl>

<dl>
<dd>

**catalog_type_id:** `str` — ID of this catalog type
    
</dd>
</dl>

<dl>
<dd>

**name:** `str` — Name is the human readable name of this entry
    
</dd>
</dl>

<dl>
<dd>

**aliases:** `typing.Optional[typing.Sequence[str]]` — Optional aliases that can be used to reference this entry
    
</dd>
</dl>

<dl>
<dd>

**external_id:** `typing.Optional[str]` — An optional alternative ID for this entry, which is ensured to be unique for the type
    
</dd>
</dl>

<dl>
<dd>

**rank:** `typing.Optional[int]` — When catalog type is ranked, this is used to help order things
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.catalog_v2.<a href="src/fern/catalog_v2/client.py">showentry</a>(...) -&gt; AsyncHttpResponse[CatalogShowEntryResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Show a single catalog entry.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.catalog_v2.showentry(
    id="01FCNDV6P870EA6S7TK1DSYDG0",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — ID of this catalog entry
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.catalog_v2.<a href="src/fern/catalog_v2/client.py">updateentry</a>(...) -&gt; AsyncHttpResponse[CatalogUpdateEntryResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Updates an existing catalog entry.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import (
    EngineParamBindingPayloadV2,
    EngineParamBindingValuePayloadV2,
    IncidentIO,
)

client = IncidentIO()
client.catalog_v2.updateentry(
    id="01FCNDV6P870EA6S7TK1DSYDG0",
    aliases=["lawrence@incident.io", "lawrence"],
    attribute_values={
        "abc123": EngineParamBindingPayloadV2(
            array_value=[
                EngineParamBindingValuePayloadV2(
                    literal="SEV123",
                    reference="incident.severity",
                )
            ],
            value=EngineParamBindingValuePayloadV2(
                literal="SEV123",
                reference="incident.severity",
            ),
        )
    },
    external_id="761722cd-d1d7-477b-ac7e-90f9e079dc33",
    name="Primary On-call",
    rank=3,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — ID of this catalog entry
    
</dd>
</dl>

<dl>
<dd>

**attribute_values:** `typing.Dict[str, EngineParamBindingPayloadV2]` — Values of this entry
    
</dd>
</dl>

<dl>
<dd>

**name:** `str` — Name is the human readable name of this entry
    
</dd>
</dl>

<dl>
<dd>

**aliases:** `typing.Optional[typing.Sequence[str]]` — Optional aliases that can be used to reference this entry
    
</dd>
</dl>

<dl>
<dd>

**external_id:** `typing.Optional[str]` — An optional alternative ID for this entry, which is ensured to be unique for the type
    
</dd>
</dl>

<dl>
<dd>

**rank:** `typing.Optional[int]` — When catalog type is ranked, this is used to help order things
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.catalog_v2.<a href="src/fern/catalog_v2/client.py">destroyentry</a>(...) -&gt; AsyncHttpResponse[None]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Archives a catalog entry.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.catalog_v2.destroyentry(
    id="01FCNDV6P870EA6S7TK1DSYDG0",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — ID of this catalog entry
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.catalog_v2.<a href="src/fern/catalog_v2/client.py">listresources</a>() -&gt; AsyncHttpResponse[CatalogListResourcesResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List available engine resources for the catalog.

A resource represents a type of data that can be held within the catalog, so this
endpoint can be used to see what attribute types can be used when updating the
schema of a catalog type.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.catalog_v2.listresources()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.catalog_v2.<a href="src/fern/catalog_v2/client.py">listtypes</a>() -&gt; AsyncHttpResponse[CatalogListTypesResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List all catalog types for an organisation, including those synced from external resources.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.catalog_v2.listtypes()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.catalog_v2.<a href="src/fern/catalog_v2/client.py">createtype</a>(...) -&gt; AsyncHttpResponse[CatalogCreateTypeResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a catalog type. The schema must be updated using the UpdateTypeSchema endpoint.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.catalog_v2.createtype(
    annotations={"incident.io/catalog-importer/id": "id-of-config"},
    categories=["customer"],
    color="yellow",
    description="Represents Kubernetes clusters that we run inside of GKE.",
    icon="alert",
    name="Kubernetes Cluster",
    ranked=True,
    source_repo_url="https://github.com/my-company/incident-io-catalog",
    type_name='Custom["BackstageGroup"]',
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**description:** `str` — Human readble description of this type
    
</dd>
</dl>

<dl>
<dd>

**name:** `str` — Name is the human readable name of this type
    
</dd>
</dl>

<dl>
<dd>

**annotations:** `typing.Optional[typing.Dict[str, str]]` — Annotations that can track metadata about this type
    
</dd>
</dl>

<dl>
<dd>

**categories:** `typing.Optional[typing.Sequence[CatalogCreateTypePayloadV2CategoriesItem]]` — What categories is this type considered part of
    
</dd>
</dl>

<dl>
<dd>

**color:** `typing.Optional[CatalogCreateTypePayloadV2Color]` — Sets the display color of this type in the dashboard
    
</dd>
</dl>

<dl>
<dd>

**icon:** `typing.Optional[CatalogCreateTypePayloadV2Icon]` — Sets the display icon of this type in the dashboard
    
</dd>
</dl>

<dl>
<dd>

**ranked:** `typing.Optional[bool]` — If this type should be ranked
    
</dd>
</dl>

<dl>
<dd>

**source_repo_url:** `typing.Optional[str]` — The url of the external repository where this type is managed
    
</dd>
</dl>

<dl>
<dd>

**type_name:** `typing.Optional[str]` — The type name of this catalog type, to be used when defining attributes. This is immutable once a CatalogType has been created. For non-externally sync types, it must follow the pattern Custom["SomeName"]
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.catalog_v2.<a href="src/fern/catalog_v2/client.py">showtype</a>(...) -&gt; AsyncHttpResponse[CatalogShowTypeResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Show a single catalog type.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.catalog_v2.showtype(
    id="01FCNDV6P870EA6S7TK1DSYDG0",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — ID of this catalog type
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.catalog_v2.<a href="src/fern/catalog_v2/client.py">updatetype</a>(...) -&gt; AsyncHttpResponse[CatalogUpdateTypeResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Updates an existing catalog type. The schema must be updated using the UpdateTypeSchema endpoint.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.catalog_v2.updatetype(
    id="01FCNDV6P870EA6S7TK1DSYDG0",
    annotations={"incident.io/catalog-importer/id": "id-of-config"},
    categories=["customer"],
    color="yellow",
    description="Represents Kubernetes clusters that we run inside of GKE.",
    icon="alert",
    name="Kubernetes Cluster",
    ranked=True,
    source_repo_url="https://github.com/my-company/incident-io-catalog",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — ID of this catalog type
    
</dd>
</dl>

<dl>
<dd>

**description:** `str` — Human readble description of this type
    
</dd>
</dl>

<dl>
<dd>

**name:** `str` — Name is the human readable name of this type
    
</dd>
</dl>

<dl>
<dd>

**annotations:** `typing.Optional[typing.Dict[str, str]]` — Annotations that can track metadata about this type
    
</dd>
</dl>

<dl>
<dd>

**categories:** `typing.Optional[typing.Sequence[CatalogUpdateTypePayloadV2CategoriesItem]]` — What categories is this type considered part of
    
</dd>
</dl>

<dl>
<dd>

**color:** `typing.Optional[CatalogUpdateTypePayloadV2Color]` — Sets the display color of this type in the dashboard
    
</dd>
</dl>

<dl>
<dd>

**icon:** `typing.Optional[CatalogUpdateTypePayloadV2Icon]` — Sets the display icon of this type in the dashboard
    
</dd>
</dl>

<dl>
<dd>

**ranked:** `typing.Optional[bool]` — If this type should be ranked
    
</dd>
</dl>

<dl>
<dd>

**source_repo_url:** `typing.Optional[str]` — The url of the external repository where this type is managed
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.catalog_v2.<a href="src/fern/catalog_v2/client.py">destroytype</a>(...) -&gt; AsyncHttpResponse[None]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Archives a catalog type and associated entries.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.catalog_v2.destroytype(
    id="01FCNDV6P870EA6S7TK1DSYDG0",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — ID of this catalog type
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.catalog_v2.<a href="src/fern/catalog_v2/client.py">updatetypeschema</a>(...) -&gt; AsyncHttpResponse[CatalogUpdateTypeSchemaResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update an existing catalog types schema, adding or removing attributes.

Updating the schema is handled separately from creating and updating types, so that you don't
have to worry about dependencies between types. For example, if type A has an attribute that
relies on type B, you would have to create type B first.

By allowing the creation of types without a schema, they can be created in any order, but it
means that you need to make a separate call to this endpoint to update the schema.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import (
    CatalogTypeAttributePathItemPayloadV2,
    CatalogTypeAttributePayloadV2,
    IncidentIO,
)

client = IncidentIO()
client.catalog_v2.updatetypeschema(
    id="01FCNDV6P870EA6S7TK1DSYDG0",
    attributes=[
        CatalogTypeAttributePayloadV2(
            array=False,
            backlink_attribute="abc123",
            id="01GW2G3V0S59R238FAHPDS1R66",
            mode="",
            name="tier",
            path=[
                CatalogTypeAttributePathItemPayloadV2(
                    attribute_id="abc123",
                )
            ],
            type='Custom["Service"]',
        )
    ],
    version=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — ID of this catalog type
    
</dd>
</dl>

<dl>
<dd>

**attributes:** `typing.Sequence[CatalogTypeAttributePayloadV2]` 
    
</dd>
</dl>

<dl>
<dd>

**version:** `int` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Custom Fields V2
<details><summary><code>client.custom_fields_v2.<a href="src/fern/custom_fields_v2/client.py">list</a>() -&gt; AsyncHttpResponse[CustomFieldsListResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List all custom fields for an organisation.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.custom_fields_v2.list()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.custom_fields_v2.<a href="src/fern/custom_fields_v2/client.py">create</a>(...) -&gt; AsyncHttpResponse[CustomFieldsCreateResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new custom field
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import CustomFieldFilterByOptionsV2, IncidentIO

client = IncidentIO()
client.custom_fields_v2.create(
    catalog_type_id="01FCNDV6P870EA6S7TK1DSYDG0",
    description="Which team is impacted by this issue",
    field_type="single_select",
    filter_by=CustomFieldFilterByOptionsV2(
        catalog_attribute_id="01H2FW182TAH0NHEVBY34SCAK0",
        custom_field_id="01H2FW182TAH0NHEVBY34SCAK0",
    ),
    group_by_catalog_attribute_id="01FCNDV6P870EA6S7TK1DSYDG0",
    helptext_catalog_attribute_id="01H2FW182TAH0NHEVBY34SCAK0",
    name="Affected Team",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**description:** `str` — Description of the custom field
    
</dd>
</dl>

<dl>
<dd>

**field_type:** `CustomFieldsCreatePayloadV2FieldType` — Type of custom field
    
</dd>
</dl>

<dl>
<dd>

**name:** `str` — Human readable name for the custom field
    
</dd>
</dl>

<dl>
<dd>

**catalog_type_id:** `typing.Optional[str]` — For catalog fields, the ID of the associated catalog type
    
</dd>
</dl>

<dl>
<dd>

**filter_by:** `typing.Optional[CustomFieldFilterByOptionsV2]` 
    
</dd>
</dl>

<dl>
<dd>

**group_by_catalog_attribute_id:** `typing.Optional[str]` — For catalog fields, the ID of the attribute used to group catalog entries (if applicable)
    
</dd>
</dl>

<dl>
<dd>

**helptext_catalog_attribute_id:** `typing.Optional[str]` — Which catalog attribute provides helptext for the options
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.custom_fields_v2.<a href="src/fern/custom_fields_v2/client.py">show</a>(...) -&gt; AsyncHttpResponse[CustomFieldsShowResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a single custom field.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.custom_fields_v2.show(
    id="01FCNDV6P870EA6S7TK1DSYDG0",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — Unique identifier for the custom field
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.custom_fields_v2.<a href="src/fern/custom_fields_v2/client.py">update</a>(...) -&gt; AsyncHttpResponse[CustomFieldsUpdateResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update the details of a custom field
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import CustomFieldFilterByOptionsV2, IncidentIO

client = IncidentIO()
client.custom_fields_v2.update(
    id="01FCNDV6P870EA6S7TK1DSYDG0",
    description="Which team is impacted by this issue",
    filter_by=CustomFieldFilterByOptionsV2(
        catalog_attribute_id="01H2FW182TAH0NHEVBY34SCAK0",
        custom_field_id="01H2FW182TAH0NHEVBY34SCAK0",
    ),
    group_by_catalog_attribute_id="01FCNDV6P870EA6S7TK1DSYDG0",
    helptext_catalog_attribute_id="01H2FW182TAH0NHEVBY34SCAK0",
    name="Affected Team",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — Unique identifier for the custom field
    
</dd>
</dl>

<dl>
<dd>

**description:** `str` — Description of the custom field
    
</dd>
</dl>

<dl>
<dd>

**name:** `str` — Human readable name for the custom field
    
</dd>
</dl>

<dl>
<dd>

**filter_by:** `typing.Optional[CustomFieldFilterByOptionsV2]` 
    
</dd>
</dl>

<dl>
<dd>

**group_by_catalog_attribute_id:** `typing.Optional[str]` — For catalog fields, the ID of the attribute used to group catalog entries (if applicable)
    
</dd>
</dl>

<dl>
<dd>

**helptext_catalog_attribute_id:** `typing.Optional[str]` — Which catalog attribute provides helptext for the options
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.custom_fields_v2.<a href="src/fern/custom_fields_v2/client.py">delete</a>(...) -&gt; AsyncHttpResponse[None]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete a custom field
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.custom_fields_v2.delete(
    id="01FCNDV6P870EA6S7TK1DSYDG0",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — Unique identifier for the custom field
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Escalations V2
<details><summary><code>client.escalations_v2.<a href="src/fern/escalations_v2/client.py">createpath</a>(...) -&gt; AsyncHttpResponse[EscalationsCreatePathResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create an escalation path.

An escalation path is a series of steps that describe how a page should be escalated,
represented as graph, supporting conditional branches based on alert priority and working
intervals.

We recommend you create escalation paths in the incident.io dashboard where our path
builder makes it easy to use conditions and visualise the path.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import (
    ConditionPayloadV2,
    EngineParamBindingPayloadV2,
    EngineParamBindingValuePayloadV2,
    EscalationPathNodeIfElsePayloadV2,
    EscalationPathNodeLevelV2,
    EscalationPathNodeNotifyChannelV2,
    EscalationPathNodePayloadV2,
    EscalationPathNodeRepeatV2,
    EscalationPathRoundRobinConfigV2,
    EscalationPathTargetV2,
    IncidentIO,
    WeekdayIntervalConfigV2,
    WeekdayIntervalV2,
)

client = IncidentIO()
client.escalations_v2.createpath(
    name="Urgent Support",
    path=[
        EscalationPathNodePayloadV2(
            id="01FCNDV6P870EA6S7TK1DSYDG0",
            if_else=EscalationPathNodeIfElsePayloadV2(
                conditions=[
                    ConditionPayloadV2(
                        operation="one_of",
                        param_bindings=[
                            EngineParamBindingPayloadV2(
                                array_value=[
                                    EngineParamBindingValuePayloadV2(
                                        literal="SEV123",
                                        reference="incident.severity",
                                    )
                                ],
                                value=EngineParamBindingValuePayloadV2(
                                    literal="SEV123",
                                    reference="incident.severity",
                                ),
                            )
                        ],
                        subject="incident.severity",
                    )
                ],
                else_path=[],
                then_path=[],
            ),
            level=EscalationPathNodeLevelV2(
                ack_mode="all",
                round_robin_config=EscalationPathRoundRobinConfigV2(
                    enabled=False,
                    rotate_after_seconds=120,
                ),
                targets=[
                    EscalationPathTargetV2(
                        id="lawrencejones",
                        schedule_mode="currently_on_call",
                        type="schedule",
                        urgency="high",
                    )
                ],
                time_to_ack_interval_condition="active",
                time_to_ack_seconds=1800,
                time_to_ack_weekday_interval_config_id="01FCNDV6P870EA6S7TK1DSYDG0",
            ),
            notify_channel=EscalationPathNodeNotifyChannelV2(
                targets=[
                    EscalationPathTargetV2(
                        id="lawrencejones",
                        schedule_mode="currently_on_call",
                        type="schedule",
                        urgency="high",
                    )
                ],
                time_to_ack_interval_condition="active",
                time_to_ack_seconds=1800,
                time_to_ack_weekday_interval_config_id="01FCNDV6P870EA6S7TK1DSYDG0",
            ),
            repeat=EscalationPathNodeRepeatV2(
                repeat_times=3,
                to_node="01FCNDV6P870EA6S7TK1DSYDG0",
            ),
            type="if_else",
        )
    ],
    team_ids=["01JPQA75EPNEES4479P16P4XAB"],
    working_hours=[
        WeekdayIntervalConfigV2(
            id="abc123",
            name="abc123",
            timezone="abc123",
            weekday_intervals=[
                WeekdayIntervalV2(
                    end_time="17:00",
                    start_time="09:00",
                    weekday="monday",
                )
            ],
        )
    ],
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**name:** `str` — The name of this escalation path, for the user's reference.
    
</dd>
</dl>

<dl>
<dd>

**path:** `typing.Sequence[EscalationPathNodePayloadV2]` — The nodes that form the levels and branches of this escalation path.
    
</dd>
</dl>

<dl>
<dd>

**team_ids:** `typing.Optional[typing.Sequence[str]]` — IDs of the teams that own this escalation path. This will automatically sync escalation paths with the right teams in Catalog. If you have an escalation paths attribute on your Teams, this attribute is required.
    
</dd>
</dl>

<dl>
<dd>

**working_hours:** `typing.Optional[typing.Sequence[WeekdayIntervalConfigV2]]` — The working hours for this escalation path.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.escalations_v2.<a href="src/fern/escalations_v2/client.py">showpath</a>(...) -&gt; AsyncHttpResponse[EscalationsShowPathResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Show an escalation path.

We recommend you create escalation paths in the incident.io dashboard where our path
builder makes it easy to use conditions and visualise the path.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.escalations_v2.showpath(
    id="01FCNDV6P870EA6S7TK1DSYDG0",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — Unique identifier for this escalation path.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.escalations_v2.<a href="src/fern/escalations_v2/client.py">updatepath</a>(...) -&gt; AsyncHttpResponse[EscalationsUpdatePathResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Updates an escalation path.

We recommend you create escalation paths in the incident.io dashboard where our path
builder makes it easy to use conditions and visualise the path.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import (
    ConditionPayloadV2,
    EngineParamBindingPayloadV2,
    EngineParamBindingValuePayloadV2,
    EscalationPathNodeIfElsePayloadV2,
    EscalationPathNodeLevelV2,
    EscalationPathNodeNotifyChannelV2,
    EscalationPathNodePayloadV2,
    EscalationPathNodeRepeatV2,
    EscalationPathRoundRobinConfigV2,
    EscalationPathTargetV2,
    IncidentIO,
    WeekdayIntervalConfigV2,
    WeekdayIntervalV2,
)

client = IncidentIO()
client.escalations_v2.updatepath(
    id="01FCNDV6P870EA6S7TK1DSYDG0",
    name="Urgent Support",
    path=[
        EscalationPathNodePayloadV2(
            id="01FCNDV6P870EA6S7TK1DSYDG0",
            if_else=EscalationPathNodeIfElsePayloadV2(
                conditions=[
                    ConditionPayloadV2(
                        operation="one_of",
                        param_bindings=[
                            EngineParamBindingPayloadV2(
                                array_value=[
                                    EngineParamBindingValuePayloadV2(
                                        literal="SEV123",
                                        reference="incident.severity",
                                    )
                                ],
                                value=EngineParamBindingValuePayloadV2(
                                    literal="SEV123",
                                    reference="incident.severity",
                                ),
                            )
                        ],
                        subject="incident.severity",
                    )
                ],
                else_path=[],
                then_path=[],
            ),
            level=EscalationPathNodeLevelV2(
                ack_mode="all",
                round_robin_config=EscalationPathRoundRobinConfigV2(
                    enabled=False,
                    rotate_after_seconds=120,
                ),
                targets=[
                    EscalationPathTargetV2(
                        id="lawrencejones",
                        schedule_mode="currently_on_call",
                        type="schedule",
                        urgency="high",
                    )
                ],
                time_to_ack_interval_condition="active",
                time_to_ack_seconds=1800,
                time_to_ack_weekday_interval_config_id="01FCNDV6P870EA6S7TK1DSYDG0",
            ),
            notify_channel=EscalationPathNodeNotifyChannelV2(
                targets=[
                    EscalationPathTargetV2(
                        id="lawrencejones",
                        schedule_mode="currently_on_call",
                        type="schedule",
                        urgency="high",
                    )
                ],
                time_to_ack_interval_condition="active",
                time_to_ack_seconds=1800,
                time_to_ack_weekday_interval_config_id="01FCNDV6P870EA6S7TK1DSYDG0",
            ),
            repeat=EscalationPathNodeRepeatV2(
                repeat_times=3,
                to_node="01FCNDV6P870EA6S7TK1DSYDG0",
            ),
            type="if_else",
        )
    ],
    team_ids=["01JPQA75EPNEES4479P16P4XAB"],
    working_hours=[
        WeekdayIntervalConfigV2(
            id="abc123",
            name="abc123",
            timezone="abc123",
            weekday_intervals=[
                WeekdayIntervalV2(
                    end_time="17:00",
                    start_time="09:00",
                    weekday="monday",
                )
            ],
        )
    ],
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — Unique identifier for this escalation path.
    
</dd>
</dl>

<dl>
<dd>

**name:** `str` — The name of this escalation path, for the user's reference.
    
</dd>
</dl>

<dl>
<dd>

**path:** `typing.Sequence[EscalationPathNodePayloadV2]` — The nodes that form the levels and branches of this escalation path.
    
</dd>
</dl>

<dl>
<dd>

**team_ids:** `typing.Optional[typing.Sequence[str]]` — IDs of the teams that own this escalation path. This will automatically sync escalation paths with the right teams in Catalog. If you have an escalation paths attribute on your Teams, this attribute is required.
    
</dd>
</dl>

<dl>
<dd>

**working_hours:** `typing.Optional[typing.Sequence[WeekdayIntervalConfigV2]]` — The working hours for this escalation path.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.escalations_v2.<a href="src/fern/escalations_v2/client.py">destroypath</a>(...) -&gt; AsyncHttpResponse[None]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Archives an escalation path.

We recommend you create escalation paths in the incident.io dashboard where our path
builder makes it easy to use conditions and visualise the path.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.escalations_v2.destroypath(
    id="01FCNDV6P870EA6S7TK1DSYDG0",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — Unique identifier for this escalation path.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.escalations_v2.<a href="src/fern/escalations_v2/client.py">list</a>(...) -&gt; AsyncHttpResponse[EscalationsListResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List all escalations for your account.

This endpoint supports a number of filters, which can help find escalations matching certain
criteria.

Note that:
- Filters may be used together, and the result will be escalations that match all filters.
- All query parameters must be URI encoded.

To use this API, you will need an API key with the "View data" or "Create and manage on-call resources" permission.

### By escalation_path

Find all escalations that escalated to escalation path with id=ABC:

		curl --get 'https://api.incident.io/v2/escalations' \
			--data 'escalation_path[one_of]=ABC'

### By status

Find all escalations with a current status of "triggered":

		curl --get 'https://api.incident.io/v2/escalations' \
			--data 'status[one_of]=triggered'

Possible values are "pending", "triggered", "acked", "resolved", "expired" and "cancelled".
Escalations are in "pending" when they are in a grace period when the related alert has
been grouped in an incident.

### By alert

Find all escalations that were created by alert with id=ABC:

		curl --get 'https://api.incident.io/v2/escalations' \
			--data 'alert[one_of]=ABC'

### By created_at and updated_at
Find all escalations that follow specified date parameters for created_at and updated_at fields.
Possible values are "gte" (greater than or equal to), "lte" (less than or equal to), and
"date_range" (between two dates).
For example, to find all escalations updated after 2025-01-01:

		curl --get 'https://api.incident.io/v2/escalations' \
			--data 'updated_at[gte]=2025-01-01'

To find all escalations created between 2025-01-01 and 2025-01-31:

		curl --get 'https://api.incident.io/v2/escalations' \
            --data 'created_at[date_range]=2025-01-01~2025-01-31'
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.escalations_v2.list(
    page_size=25,
    after="01FDAG4SAP5TYPT98WGR2N7W91",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**page_size:** `typing.Optional[int]` — Number of escalations to return per page
    
</dd>
</dl>

<dl>
<dd>

**after:** `typing.Optional[str]` — An escalation's ID. This endpoint will return a list of escalations after this ID in relation to the API response order.
    
</dd>
</dl>

<dl>
<dd>

**escalation_path:** `typing.Optional[typing.Dict[str, typing.Sequence[str]]]` — Filter on the escalation path for which the escalation was triggered. Accepted operators are 'one_of' and 'not_in'.
    
</dd>
</dl>

<dl>
<dd>

**status:** `typing.Optional[typing.Dict[str, typing.Sequence[str]]]` — Filter on the status of the escalation. Accepted operators are 'one_of' and 'not_in'.
    
</dd>
</dl>

<dl>
<dd>

**alert:** `typing.Optional[typing.Dict[str, typing.Sequence[str]]]` — Filter on the alert that created an escalation. Accepted operators are 'one_of' and 'not_in'.
    
</dd>
</dl>

<dl>
<dd>

**created_at:** `typing.Optional[typing.Dict[str, typing.Sequence[str]]]` — Filter on the created_at timestamp of the escalation. Accepted operators are 'gte', 'lte' and 'date_range'.
    
</dd>
</dl>

<dl>
<dd>

**updated_at:** `typing.Optional[typing.Dict[str, typing.Sequence[str]]]` — Filter on the updated_at timestamp of the escalation. Accepted operators are 'gte', 'lte' and 'date_range'.
    
</dd>
</dl>

<dl>
<dd>

**idempotency_key:** `typing.Optional[typing.Dict[str, typing.Sequence[str]]]` — Filter on the idempotency key of the escalation. This is the key set when creating escalations via the API, and is distinct from alert deduplication keys. Accepted operators are 'is' for exact matches and 'starts_with' for prefix matching.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.escalations_v2.<a href="src/fern/escalations_v2/client.py">create</a>(...) -&gt; AsyncHttpResponse[EscalationsCreateResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create an escalation.

An escalation pages people, either according to an escalation path, or directly to
specific users. You must provide either an escalation_path_id OR user_ids, but not both.

When escalating via an escalation path, the escalation will follow the configured path
with its levels and timeouts, using your default [alert
priority](https://app.incident.io/~/settings/alerts/configuration/priorities).

When escalating directly to users, they will receive a high-urgency
notification, based on their notification rules.

This endpoint is rate-limited to 60 requests per minute, since it is intended for
interactive use cases (for example someone clicking a "escalate to team" button
in your internal developer platform). To escalate based on automated alerts, we
recommend sending events to an alert source instead.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.escalations_v2.create(
    description="Database CPU has been above 90% for 5 minutes",
    escalation_path_id="01H0J1EXE7AXZ2C93K61WBPYEH",
    idempotency_key="2024-01-15-abc123",
    title="Production database experiencing high CPU",
    user_ids=["01H0J1EXE7AXZ2C93K61WBPYEH", "01H0J1EXE7AXZ2C93K61WBPYEI"],
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**idempotency_key:** `str` — Unique key to prevent duplicate escalations. If this key has already been used, the existing escalation will be returned.
    
</dd>
</dl>

<dl>
<dd>

**title:** `str` — The title of the escalation. This message will be included in all notifications about this escalation.
    
</dd>
</dl>

<dl>
<dd>

**description:** `typing.Optional[str]` — Additional details about the escalation
    
</dd>
</dl>

<dl>
<dd>

**escalation_path_id:** `typing.Optional[str]` — ID of the escalation path to follow
    
</dd>
</dl>

<dl>
<dd>

**user_ids:** `typing.Optional[typing.Sequence[str]]` — IDs of users to escalate directly to
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.escalations_v2.<a href="src/fern/escalations_v2/client.py">show</a>(...) -&gt; AsyncHttpResponse[EscalationsShowResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Show a specific escalation.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.escalations_v2.show(
    id="01G0J1EXE7AXZ2C93K61WBPYEH",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — Unique ID of the escalation
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Follow-ups V2
<details><summary><code>client.follow_ups_v2.<a href="src/fern/follow_ups_v2/client.py">list</a>(...) -&gt; AsyncHttpResponse[FollowUpsListResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List all follow-ups for an organisation.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.follow_ups_v2.list(
    incident_id="01FCNDV6P870EA6S7TK1DSYDG0",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**incident_id:** `typing.Optional[str]` — Find follow-ups related to this incident
    
</dd>
</dl>

<dl>
<dd>

**incident_mode:** `typing.Optional[FollowUpsV2ListRequestIncidentMode]` — Filter to follow-ups from incidents of the given mode. If not set, only follow-ups from `standard` and `retrospective` incidents are returned
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.follow_ups_v2.<a href="src/fern/follow_ups_v2/client.py">show</a>(...) -&gt; AsyncHttpResponse[FollowUpsShowResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a single incident follow-up.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.follow_ups_v2.show(
    id="01FCNDV6P870EA6S7TK1DSYDG0",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — Unique identifier for the follow-up
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Incident Roles V2
<details><summary><code>client.incident_roles_v2.<a href="src/fern/incident_roles_v2/client.py">list</a>() -&gt; AsyncHttpResponse[IncidentRolesListResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List all incident roles for an organisation.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.incident_roles_v2.list()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.incident_roles_v2.<a href="src/fern/incident_roles_v2/client.py">create</a>(...) -&gt; AsyncHttpResponse[IncidentRolesCreateResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new incident role
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.incident_roles_v2.create(
    description="The person currently coordinating the incident",
    instructions="Take point on the incident; Make sure people are clear on responsibilities",
    name="Incident Lead",
    shortform="lead",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**description:** `str` — Describes the purpose of the role
    
</dd>
</dl>

<dl>
<dd>

**instructions:** `str` — Provided to whoever is nominated for the role. Note that this will be empty for the 'reporter' role.
    
</dd>
</dl>

<dl>
<dd>

**name:** `str` — Human readable name of the incident role
    
</dd>
</dl>

<dl>
<dd>

**shortform:** `str` — Short human readable name for Slack. Note that this will be empty for the 'reporter' role.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.incident_roles_v2.<a href="src/fern/incident_roles_v2/client.py">show</a>(...) -&gt; AsyncHttpResponse[IncidentRolesShowResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a single incident role.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.incident_roles_v2.show(
    id="01FCNDV6P870EA6S7TK1DSYDG0",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — Unique identifier for the role
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.incident_roles_v2.<a href="src/fern/incident_roles_v2/client.py">update</a>(...) -&gt; AsyncHttpResponse[IncidentRolesUpdateResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update an existing incident role
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.incident_roles_v2.update(
    id="01FCNDV6P870EA6S7TK1DSYDG0",
    description="The person currently coordinating the incident",
    instructions="Take point on the incident; Make sure people are clear on responsibilities",
    name="Incident Lead",
    shortform="lead",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — Unique identifier for the role
    
</dd>
</dl>

<dl>
<dd>

**description:** `str` — Describes the purpose of the role
    
</dd>
</dl>

<dl>
<dd>

**instructions:** `str` — Provided to whoever is nominated for the role. Note that this will be empty for the 'reporter' role.
    
</dd>
</dl>

<dl>
<dd>

**name:** `str` — Human readable name of the incident role
    
</dd>
</dl>

<dl>
<dd>

**shortform:** `str` — Short human readable name for Slack. Note that this will be empty for the 'reporter' role.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.incident_roles_v2.<a href="src/fern/incident_roles_v2/client.py">delete</a>(...) -&gt; AsyncHttpResponse[None]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Removes an existing role
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.incident_roles_v2.delete(
    id="01FCNDV6P870EA6S7TK1DSYDG0",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — Unique identifier for the role
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Incident Timestamps V2
<details><summary><code>client.incident_timestamps_v2.<a href="src/fern/incident_timestamps_v2/client.py">list</a>() -&gt; AsyncHttpResponse[IncidentTimestampsListResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List all incident timestamps for an organisation.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.incident_timestamps_v2.list()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.incident_timestamps_v2.<a href="src/fern/incident_timestamps_v2/client.py">show</a>(...) -&gt; AsyncHttpResponse[IncidentTimestampsShowResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a single incident timestamp.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.incident_timestamps_v2.show(
    id="01FCNDV6P870EA6S7TK1DSYD5H",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — Unique ID of this incident timestamp
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Incident Updates V2
<details><summary><code>client.incident_updates_v2.<a href="src/fern/incident_updates_v2/client.py">list</a>(...) -&gt; AsyncHttpResponse[IncidentUpdatesListResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List all incident updates for an organisation, or for a specific incident.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.incident_updates_v2.list(
    incident_id="01G0J1EXE7AXZ2C93K61WBPYEH",
    page_size=25,
    after="01FDAG4SAP5TYPT98WGR2N7W91",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**incident_id:** `typing.Optional[str]` — Incident whose updates you want to list
    
</dd>
</dl>

<dl>
<dd>

**page_size:** `typing.Optional[int]` — Integer number of records to return
    
</dd>
</dl>

<dl>
<dd>

**after:** `typing.Optional[str]` — An record's ID. This endpoint will return a list of records after this ID in relation to the API response order.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Incidents V2
<details><summary><code>client.incidents_v2.<a href="src/fern/incidents_v2/client.py">list</a>(...) -&gt; AsyncHttpResponse[IncidentsListResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List all incidents for an organisation.

This endpoint supports a number of filters, which can help find incidents matching certain
criteria.

Filters are provided as query parameters, but due to the dynamic nature of what you can
query by (different accounts have different custom fields, statuses, etc) they are more
complex than most.

The maximum page size that can be requested is 250.

To help, here are some exemplar curl requests with a human description of what they search
for.

Note that:
- Filters may be combined using the filter_mode parameter: 'all' (default) requires all filters
to match (AND logic), while 'any' requires at least one filter to match (OR logic).
- IDs are normally in UUID format, but have been replaced with shorter strings to improve
readability.
- All query parameters must be URI encoded.

### By status

With status of id=ABC, find all incidents that are set to that status:

		curl --get 'https://api.incident.io/v2/incidents' \
			--data 'status[one_of]=ABC'

Or all incidents that are not set to status with id=ABC:

		curl --get 'https://api.incident.io/v2/incidents' \
			--data 'status[not_in]=ABC'

### By created_at or updated_at

Find all incidents that follow specified date parameters for created_at and updated_at fields.
Possible values are "gte" (greater than or equal to), "lte" (less than or equal to), and
"date_range" (between two dates). The following example finds all incidents created before
or on 2021-01-02T00:00:00Z:

		curl --get 'https://api.incident.io/v2/incidents' \
			--data 'created_at[lte]=2021-01-02'

To find incidents created within a specific date range, use the date_range option with
tilde-separated dates:

		curl --get 'https://api.incident.io/v2/incidents' \
			--data 'created_at[date_range]=2024-12-02~2024-12-08'

### By status category

Find all incidents that are in a status category. Possible values are "triage",
"declined", "merged", "canceled", "live", "learning" and "closed":

		curl --get 'https://api.incident.io/v2/incidents' \
			--data 'status_category[one_of]=live'

Or all incidents that are not in a status category:

		curl --get 'https://api.incident.io/v2/incidents' \
			--data 'status_category[not_in]=live'


### By severity

With severity of id=ABC, find all incidents that are set to that severity:

		curl --get 'https://api.incident.io/v2/incidents' \
			--data 'severity[one_of]=ABC'

Or all incidents where severity rank is greater-than-or-equal-to the rank of severity
id=ABC:

		curl --get 'https://api.incident.io/v2/incidents' \
			--data 'severity[gte]=ABC'

Or all incidents where severity rank is less-than-or-equal-to the rank of severity id=ABC:

		curl --get 'https://api.incident.io/v2/incidents' \
			--data 'severity[lte]=ABC'

### By incident type

With incident type of id=ABC, find all incidents that are of that type:

		curl --get 'https://api.incident.io/v2/incidents' \
			--data 'incident_type[one_of]=ABC'

Or all incidents not of that type:

		curl --get 'https://api.incident.io/v2/incidents' \
			--data 'incident_type[not_in]=ABC'

### By incident mode

By default, we return standard and retrospective incidents. This means that test and
tutorial incidents are filtered out. To override this behaviour, you can use the
mode filter to specify which modes you want to get.

To find incidents of all modes:

		curl --get 'https://api.incident.io/v2/incidents' \
			--data 'mode[one_of]=standard&mode[one_of]=retrospective&mode[one_of]=test&mode[one_of]=tutorial'

To find just test incidents:

		curl --get 'https://api.incident.io/v2/incidents' \
			--data 'mode[one_of]=test'


### By incident role

Roles and custom fields have another nested layer in the query parameter, to account for
operations against any of the roles or custom fields created in the account.

With incident role id=ABC, find all incidents where that role is unset:

		curl --get 'https://api.incident.io/v2/incidents' \
			--data 'incident_role[ABC][is_set]=true'

Or where the role has been set:

		curl --get 'https://api.incident.io/v2/incidents' \
			--data 'incident_role[ABC][is_set]=false'

### By option custom fields

With an option custom field id=ABC, all incidents that have field ABC set to the custom
field option of id=XYZ:

		curl \
			--get 'https://api.incident.io/v2/incidents' \
			--data 'custom_field[ABC][one_of]=XYZ'

Or all incidents that do not have custom field id=ABC set to option id=XYZ:

		curl \
			--get 'https://api.incident.io/v2/incidents' \
			--data 'custom_field[ABC][not_in]=XYZ'
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.incidents_v2.list(
    page_size=25,
    after="01FDAG4SAP5TYPT98WGR2N7W91",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**page_size:** `typing.Optional[int]` — Integer number of records to return
    
</dd>
</dl>

<dl>
<dd>

**after:** `typing.Optional[str]` — An incident's ID. This endpoint will return a list of incidents after this ID in relation to the API response order.
    
</dd>
</dl>

<dl>
<dd>

**filter_mode:** `typing.Optional[IncidentsV2ListRequestFilterMode]` — How to combine the filters: 'all' combines them with AND logic (all must match), 'any' combines them with OR logic (any can match). Defaults to 'all'.
    
</dd>
</dl>

<dl>
<dd>

**status:** `typing.Optional[typing.Dict[str, typing.Sequence[str]]]` — Filter on incident status. The accepted operators are 'one_of', or 'not_in'.
    
</dd>
</dl>

<dl>
<dd>

**status_category:** `typing.Optional[typing.Dict[str, typing.Sequence[str]]]` — Filter on the category of the incidents status. The accepted operators are 'one_of', or 'not_in'.
    
</dd>
</dl>

<dl>
<dd>

**created_at:** `typing.Optional[typing.Dict[str, typing.Sequence[str]]]` — Filter on incident created at timestamp. The accepted operators are 'gte', 'lte' and 'date_range'.
    
</dd>
</dl>

<dl>
<dd>

**updated_at:** `typing.Optional[typing.Dict[str, typing.Sequence[str]]]` — Filter on incident updated at timestamp. The accepted operators are 'gte', 'lte' and 'date_range'.
    
</dd>
</dl>

<dl>
<dd>

**severity:** `typing.Optional[typing.Dict[str, typing.Sequence[str]]]` — Filter on incident severity. The accepted operators are 'one_of', 'not_in', 'gte', 'lte'.
    
</dd>
</dl>

<dl>
<dd>

**incident_type:** `typing.Optional[typing.Dict[str, typing.Sequence[str]]]` — Filter on incident type. The accepted operators are 'one_of, or 'not_in'.
    
</dd>
</dl>

<dl>
<dd>

**incident_role:** `typing.Optional[typing.Dict[str, typing.Dict[str, typing.Sequence[str]]]]` — Filter on an incident role. Role ID should be sent, followed by the operator and values. The accepted operators are 'one_of', 'is_blank'.
    
</dd>
</dl>

<dl>
<dd>

**custom_field:** `typing.Optional[typing.Dict[str, typing.Dict[str, typing.Sequence[str]]]]` — Filter on an incident custom field. Custom field ID should be sent, followed by the operator and values. Accepted operator will depend on the custom field type.
    
</dd>
</dl>

<dl>
<dd>

**mode:** `typing.Optional[typing.Dict[str, typing.Sequence[str]]]` — Filter on incident mode. The accepted operator is 'one_of'.  If this is not provided, this value defaults to `{"one_of": ["standard", "retrospective"] }`, meaning that test and tutorial incidents are not included.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.incidents_v2.<a href="src/fern/incidents_v2/client.py">create</a>(...) -&gt; AsyncHttpResponse[IncidentsCreateResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new incident.

Note that if the incident mode is set to "retrospective" then the new incident
will not be announced in Slack.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
import datetime

from fern import (
    CustomFieldEntryPayloadV2,
    CustomFieldValuePayloadV2,
    IncidentIO,
    IncidentRoleAssignmentPayloadV2,
    IncidentTimestampValuePayloadV2,
    RetrospectiveIncidentOptionsV2,
    UserReferencePayloadV2,
)

client = IncidentIO()
client.incidents_v2.create(
    custom_field_entries=[
        CustomFieldEntryPayloadV2(
            custom_field_id="01FCNDV6P870EA6S7TK1DSYDG0",
            values=[
                CustomFieldValuePayloadV2(
                    id="01FCNDV6P870EA6S7TK1DSYDG0",
                    value_catalog_entry_id="01FCNDV6P870EA6S7TK1DSYDG0",
                    value_link="https://google.com/",
                    value_numeric="123.456",
                    value_option_id="01FCNDV6P870EA6S7TK1DSYDG0",
                    value_text="This is my text field, I hope you like it",
                    value_timestamp="",
                )
            ],
        )
    ],
    idempotency_key="alert-uuid",
    incident_role_assignments=[
        IncidentRoleAssignmentPayloadV2(
            assignee=UserReferencePayloadV2(
                email="bob@example.com",
                id="01G0J1EXE7AXZ2C93K61WBPYEH",
                slack_user_id="USER123",
            ),
            incident_role_id="01FH5TZRWMNAFB0DZ23FD1TV96",
        )
    ],
    incident_status_id="01G0J1EXE7AXZ2C93K61WBPYEH",
    incident_timestamp_values=[
        IncidentTimestampValuePayloadV2(
            incident_timestamp_id="01FCNDV6P870EA6S7TK1DSYD5H",
            value=datetime.datetime.fromisoformat(
                "2021-08-17 13:28:57+00:00",
            ),
        )
    ],
    incident_type_id="01FH5TZRWMNAFB0DZ23FD1TV96",
    mode="standard",
    name="Our database is sad",
    retrospective_incident_options=RetrospectiveIncidentOptionsV2(
        external_id=123,
        postmortem_document_url="https://docs.google.com/my_doc_id",
        slack_channel_id="abc123",
    ),
    severity_id="01FH5TZRWMNAFB0DZ23FD1TV96",
    slack_channel_name_override="inc-123-database-down",
    slack_team_id="T02A1FSLE8J",
    summary="Our database is really really sad, and we don't know why yet.",
    visibility="public",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**idempotency_key:** `str` — Unique string used to de-duplicate incident create requests
    
</dd>
</dl>

<dl>
<dd>

**visibility:** `IncidentsCreatePayloadV2Visibility` — Whether the incident should be open to anyone in your Slack workspace (public), or invite-only (private). For more information on Private Incidents see our [help centre](https://help.incident.io/articles/5905558102-can-we-mark-incidents-as-sensitive-and-restrict-access).
    
</dd>
</dl>

<dl>
<dd>

**custom_field_entries:** `typing.Optional[typing.Sequence[CustomFieldEntryPayloadV2]]` — Set the incident's custom fields to these values
    
</dd>
</dl>

<dl>
<dd>

**incident_role_assignments:** `typing.Optional[typing.Sequence[IncidentRoleAssignmentPayloadV2]]` — Assign incident roles to these people
    
</dd>
</dl>

<dl>
<dd>

**incident_status_id:** `typing.Optional[str]` — Incident status to assign to the incident
    
</dd>
</dl>

<dl>
<dd>

**incident_timestamp_values:** `typing.Optional[typing.Sequence[IncidentTimestampValuePayloadV2]]` — Assign the incident's timestamps to these values
    
</dd>
</dl>

<dl>
<dd>

**incident_type_id:** `typing.Optional[str]` — Incident type to create this incident as
    
</dd>
</dl>

<dl>
<dd>

**mode:** `typing.Optional[IncidentsCreatePayloadV2Mode]` — Whether the incident is real, a test, a tutorial, or importing as a retrospective incident
    
</dd>
</dl>

<dl>
<dd>

**name:** `typing.Optional[str]` — Explanation of the incident
    
</dd>
</dl>

<dl>
<dd>

**retrospective_incident_options:** `typing.Optional[RetrospectiveIncidentOptionsV2]` 
    
</dd>
</dl>

<dl>
<dd>

**severity_id:** `typing.Optional[str]` — Severity to create incident as
    
</dd>
</dl>

<dl>
<dd>

**slack_channel_name_override:** `typing.Optional[str]` — Name of the Slack channel to create for this incident
    
</dd>
</dl>

<dl>
<dd>

**slack_team_id:** `typing.Optional[str]` — Slack Team to create the incident in
    
</dd>
</dl>

<dl>
<dd>

**summary:** `typing.Optional[str]` — Detailed description of the incident
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.incidents_v2.<a href="src/fern/incidents_v2/client.py">show</a>(...) -&gt; AsyncHttpResponse[IncidentsShowResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a single incident.

The ID supplied can be either the incident's full ID, or the numeric part of its
reference. For example, to get INC-123, you could use either its full ID or:

		curl \
			--get 'https://api.incident.io/v2/incidents/123
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.incidents_v2.show(
    id="01FDAG4SAP5TYPT98WGR2N7W91",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — Unique identifier for the incident
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.incidents_v2.<a href="src/fern/incidents_v2/client.py">edit</a>(...) -&gt; AsyncHttpResponse[IncidentsEditResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Edit an existing incident.

This endpoint allows you to edit the properties of an existing incident: e.g. set the severity or update custom fields.

When using this endpoint, only fields that are provided will be edited (omitted fields
will be ignored).
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
import datetime

from fern import (
    CustomFieldEntryPayloadV2,
    CustomFieldValuePayloadV2,
    IncidentEditPayloadV2,
    IncidentIO,
    IncidentRoleAssignmentPayloadV2,
    IncidentTimestampValuePayloadV2,
    UserReferencePayloadV2,
)

client = IncidentIO()
client.incidents_v2.edit(
    id="01G18REBY9AYH6CMWCJ2CVCYCH",
    incident=IncidentEditPayloadV2(
        call_url="https://zoom.us/foo",
        custom_field_entries=[
            CustomFieldEntryPayloadV2(
                custom_field_id="01FCNDV6P870EA6S7TK1DSYDG0",
                values=[
                    CustomFieldValuePayloadV2(
                        id="01FCNDV6P870EA6S7TK1DSYDG0",
                        value_catalog_entry_id="01FCNDV6P870EA6S7TK1DSYDG0",
                        value_link="https://google.com/",
                        value_numeric="123.456",
                        value_option_id="01FCNDV6P870EA6S7TK1DSYDG0",
                        value_text="This is my text field, I hope you like it",
                        value_timestamp="",
                    )
                ],
            )
        ],
        incident_role_assignments=[
            IncidentRoleAssignmentPayloadV2(
                assignee=UserReferencePayloadV2(
                    email="bob@example.com",
                    id="01G0J1EXE7AXZ2C93K61WBPYEH",
                    slack_user_id="USER123",
                ),
                incident_role_id="01FH5TZRWMNAFB0DZ23FD1TV96",
            )
        ],
        incident_status_id="abc123",
        incident_timestamp_values=[
            IncidentTimestampValuePayloadV2(
                incident_timestamp_id="01FCNDV6P870EA6S7TK1DSYD5H",
                value=datetime.datetime.fromisoformat(
                    "2021-08-17 13:28:57+00:00",
                ),
            )
        ],
        name="Our database is sad",
        severity_id="01G0J1EXE7AXZ2C93K61WBPYEH",
        slack_channel_name_override="inc-123-database-down",
        summary="Our database is really really sad, and we don't know why yet.",
    ),
    notify_incident_channel=True,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — The unique identifier of the incident that you want to edit
    
</dd>
</dl>

<dl>
<dd>

**incident:** `IncidentEditPayloadV2` 
    
</dd>
</dl>

<dl>
<dd>

**notify_incident_channel:** `bool` — Should we send Slack channel notifications to inform responders of this update? Note that this won't work if the Slack channel has already been archived.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Schedules V2
<details><summary><code>client.schedules_v2.<a href="src/fern/schedules_v2/client.py">listscheduleentries</a>(...) -&gt; AsyncHttpResponse[SchedulesListScheduleEntriesResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a list of schedule entries. The endpoint will return all entries that overlap with the given window, if one is provided.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
import datetime

from fern import IncidentIO

client = IncidentIO()
client.schedules_v2.listscheduleentries(
    schedule_id="01FDAG4SAP5TYPT98WGR2N7W91",
    entry_window_start=datetime.datetime.fromisoformat(
        "2021-01-01 00:00:00+00:00",
    ),
    entry_window_end=datetime.datetime.fromisoformat(
        "2021-01-01 00:00:00+00:00",
    ),
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**schedule_id:** `str` — The ID of the schedule to get entries for.
    
</dd>
</dl>

<dl>
<dd>

**entry_window_start:** `typing.Optional[dt.datetime]` — The start of the window to get entries for.
    
</dd>
</dl>

<dl>
<dd>

**entry_window_end:** `typing.Optional[dt.datetime]` — The end of the window to get entries for.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.schedules_v2.<a href="src/fern/schedules_v2/client.py">createoverride</a>(...) -&gt; AsyncHttpResponse[SchedulesCreateOverrideResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new schedule override.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
import datetime

from fern import IncidentIO, UserReferencePayloadV2

client = IncidentIO()
client.schedules_v2.createoverride(
    end_at=datetime.datetime.fromisoformat(
        "2021-08-17 14:00:00+00:00",
    ),
    layer_id="01G0J1EXE7AXZ2C93K61WBPYNH",
    rotation_id="01G0J1EXE7AXZ2C93K61WBPYEH",
    schedule_id="01G0J1EXE7AXZ2C93K61WBPYEH",
    start_at=datetime.datetime.fromisoformat(
        "2021-08-17 13:00:00+00:00",
    ),
    user=UserReferencePayloadV2(
        email="bob@example.com",
        id="01G0J1EXE7AXZ2C93K61WBPYEH",
        slack_user_id="USER123",
    ),
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**end_at:** `dt.datetime` — End time of the override
    
</dd>
</dl>

<dl>
<dd>

**layer_id:** `str` — The layer this override applies to
    
</dd>
</dl>

<dl>
<dd>

**rotation_id:** `str` — The rotation this override applies to
    
</dd>
</dl>

<dl>
<dd>

**schedule_id:** `str` — The schedule this override applies to
    
</dd>
</dl>

<dl>
<dd>

**start_at:** `dt.datetime` — Start time of the override
    
</dd>
</dl>

<dl>
<dd>

**user:** `UserReferencePayloadV2` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.schedules_v2.<a href="src/fern/schedules_v2/client.py">list</a>(...) -&gt; AsyncHttpResponse[SchedulesListResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List configured schedules.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.schedules_v2.list(
    page_size=25,
    after="01FDAG4SAP5TYPT98WGR2N7W91",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**page_size:** `typing.Optional[int]` — Integer number of records to return
    
</dd>
</dl>

<dl>
<dd>

**after:** `typing.Optional[str]` — A schedule's ID. This endpoint will return a list of schedules after this ID in relation to the API response order.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.schedules_v2.<a href="src/fern/schedules_v2/client.py">create</a>(...) -&gt; AsyncHttpResponse[SchedulesCreateResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new schedule.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
import datetime

from fern import (
    IncidentIO,
    ScheduleConfigCreatePayloadV2,
    ScheduleCreatePayloadV2,
    ScheduleHolidaysPublicConfigPayloadV2,
    ScheduleLayerCreatePayloadV2,
    ScheduleRotationCreatePayloadV2,
    ScheduleRotationHandoverV2,
    ScheduleRotationWorkingIntervalCreatePayloadV2,
    UserReferencePayloadV2,
)

client = IncidentIO()
client.schedules_v2.create(
    schedule=ScheduleCreatePayloadV2(
        annotations={"incident.io/terraform/version": "version-of-terraform"},
        config=ScheduleConfigCreatePayloadV2(
            rotations=[
                ScheduleRotationCreatePayloadV2(
                    effective_from=datetime.datetime.fromisoformat(
                        "2021-08-17 13:28:57+00:00",
                    ),
                    handover_start_at=datetime.datetime.fromisoformat(
                        "2021-08-17 13:28:57+00:00",
                    ),
                    handovers=[
                        ScheduleRotationHandoverV2(
                            interval=1,
                            interval_type="hourly",
                        )
                    ],
                    id="01G0J1EXE7AXZ2C93K61WBPYEH",
                    layers=[
                        ScheduleLayerCreatePayloadV2(
                            id="01G0J1EXE7AXZ2C93K61WBPYEH",
                            name="Layer 1",
                        )
                    ],
                    name="My Rotation",
                    scheduling_mode="fair",
                    users=[
                        UserReferencePayloadV2(
                            email="bob@example.com",
                            id="01G0J1EXE7AXZ2C93K61WBPYEH",
                            slack_user_id="USER123",
                        )
                    ],
                    working_interval=[
                        ScheduleRotationWorkingIntervalCreatePayloadV2(
                            end_time="17:00",
                            start_time="09:00",
                            weekday="monday",
                        )
                    ],
                )
            ],
        ),
        holidays_public_config=ScheduleHolidaysPublicConfigPayloadV2(
            country_codes=["abc123"],
        ),
        name="Primary On-call Schedule",
        team_ids=["01JPQA75EPNEES4479P16P4XAB"],
        timezone="America/Los_Angeles",
    ),
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**schedule:** `ScheduleCreatePayloadV2` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.schedules_v2.<a href="src/fern/schedules_v2/client.py">show</a>(...) -&gt; AsyncHttpResponse[SchedulesShowResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a single schedule.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.schedules_v2.show(
    id="01G0J1EXE7AXZ2C93K61WBPYEH",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — Unique internal ID of the schedule
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.schedules_v2.<a href="src/fern/schedules_v2/client.py">update</a>(...) -&gt; AsyncHttpResponse[SchedulesUpdateResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update a schedule.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
import datetime

from fern import (
    IncidentIO,
    ScheduleConfigUpdatePayloadV2,
    ScheduleHolidaysPublicConfigPayloadV2,
    ScheduleLayerUpdatePayloadV2,
    ScheduleRotationHandoverV2,
    ScheduleRotationUpdatePayloadV2,
    ScheduleRotationWorkingIntervalV2,
    ScheduleUpdatePayloadV2,
    UserReferencePayloadV2,
)

client = IncidentIO()
client.schedules_v2.update(
    id="01G0J1EXE7AXZ2C93K61WBPYEH",
    schedule=ScheduleUpdatePayloadV2(
        annotations={"incident.io/terraform/version": "version-of-terraform"},
        config=ScheduleConfigUpdatePayloadV2(
            rotations=[
                ScheduleRotationUpdatePayloadV2(
                    effective_from=datetime.datetime.fromisoformat(
                        "2021-08-17 13:28:57+00:00",
                    ),
                    handover_start_at=datetime.datetime.fromisoformat(
                        "2021-08-17 13:28:57+00:00",
                    ),
                    handovers=[
                        ScheduleRotationHandoverV2(
                            interval=1,
                            interval_type="hourly",
                        )
                    ],
                    id="01G0J1EXE7AXZ2C93K61WBPYEH",
                    layers=[
                        ScheduleLayerUpdatePayloadV2(
                            id="01G0J1EXE7AXZ2C93K61WBPYEH",
                            name="Layer 1",
                        )
                    ],
                    name="My Rotation",
                    scheduling_mode="fair",
                    users=[
                        UserReferencePayloadV2(
                            email="bob@example.com",
                            id="01G0J1EXE7AXZ2C93K61WBPYEH",
                            slack_user_id="USER123",
                        )
                    ],
                    working_interval=[
                        ScheduleRotationWorkingIntervalV2(
                            end_time="17:00",
                            start_time="09:00",
                            weekday="monday",
                        )
                    ],
                )
            ],
        ),
        holidays_public_config=ScheduleHolidaysPublicConfigPayloadV2(
            country_codes=["abc123"],
        ),
        name="Primary On-call Schedule",
        team_ids=["01JPQA75EPNEES4479P16P4XAB"],
        timezone="America/Los_Angeles",
    ),
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — The schedule ID to update.
    
</dd>
</dl>

<dl>
<dd>

**schedule:** `ScheduleUpdatePayloadV2` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.schedules_v2.<a href="src/fern/schedules_v2/client.py">destroy</a>(...) -&gt; AsyncHttpResponse[None]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Archives a single schedule.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.schedules_v2.destroy(
    id="01G0J1EXE7AXZ2C93K61WBPYEH",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — Unique internal ID of the schedule
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Users V2
<details><summary><code>client.users_v2.<a href="src/fern/users_v2/client.py">list</a>(...) -&gt; AsyncHttpResponse[UsersListResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List users in your account.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.users_v2.list(
    email="john.doe@incident.io",
    slack_user_id="U12345678",
    page_size=25,
    after="01FDAG4SAP5TYPT98WGR2N7W91",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**email:** `typing.Optional[str]` — Filter by email address
    
</dd>
</dl>

<dl>
<dd>

**slack_user_id:** `typing.Optional[str]` — Filter by Slack user ID
    
</dd>
</dl>

<dl>
<dd>

**page_size:** `typing.Optional[int]` — Integer number of records to return
    
</dd>
</dl>

<dl>
<dd>

**after:** `typing.Optional[str]` — An record's ID. This endpoint will return a list of records after this ID in relation to the API response order.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.users_v2.<a href="src/fern/users_v2/client.py">show</a>(...) -&gt; AsyncHttpResponse[UsersShowResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get a single user.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.users_v2.show(
    id="01FCNDV6P870EA6S7TK1DSYDG0",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — Unique identifier of the user
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Workflows V2
<details><summary><code>client.workflows_v2.<a href="src/fern/workflows_v2/client.py">listworkflows</a>() -&gt; AsyncHttpResponse[WorkflowsListWorkflowsResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List all workflows
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.workflows_v2.listworkflows()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.workflows_v2.<a href="src/fern/workflows_v2/client.py">createworkflow</a>(...) -&gt; AsyncHttpResponse[WorkflowsCreateWorkflowResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new workflow
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import (
    ConditionGroupPayloadV2,
    ConditionPayloadV2,
    EngineParamBindingPayloadV2,
    EngineParamBindingValuePayloadV2,
    ExpressionBranchesOptsPayloadV2,
    ExpressionBranchPayloadV2,
    ExpressionConcatenateOptsPayloadV2,
    ExpressionElseBranchPayloadV2,
    ExpressionFilterOptsPayloadV2,
    ExpressionNavigateOptsPayloadV2,
    ExpressionOperationPayloadV2,
    ExpressionParseOptsPayloadV2,
    ExpressionPayloadV2,
    IncidentIO,
    ReturnsMetaV2,
    StepConfigPayloadV2,
    WorkflowDelayV2,
)

client = IncidentIO()
client.workflows_v2.createworkflow(
    annotations={"incident.io/terraform/version": "3.0.0"},
    condition_groups=[
        ConditionGroupPayloadV2(
            conditions=[
                ConditionPayloadV2(
                    operation="one_of",
                    param_bindings=[
                        EngineParamBindingPayloadV2(
                            array_value=[
                                EngineParamBindingValuePayloadV2(
                                    literal="SEV123",
                                    reference="incident.severity",
                                )
                            ],
                            value=EngineParamBindingValuePayloadV2(
                                literal="SEV123",
                                reference="incident.severity",
                            ),
                        )
                    ],
                    subject="incident.severity",
                )
            ],
        )
    ],
    continue_on_step_error=True,
    delay=WorkflowDelayV2(
        conditions_apply_over_delay=False,
        for_seconds=60,
    ),
    expressions=[
        ExpressionPayloadV2(
            else_branch=ExpressionElseBranchPayloadV2(
                result=EngineParamBindingPayloadV2(
                    array_value=[
                        EngineParamBindingValuePayloadV2(
                            literal="SEV123",
                            reference="incident.severity",
                        )
                    ],
                    value=EngineParamBindingValuePayloadV2(
                        literal="SEV123",
                        reference="incident.severity",
                    ),
                ),
            ),
            label="Team Slack channel",
            operations=[
                ExpressionOperationPayloadV2(
                    branches=ExpressionBranchesOptsPayloadV2(
                        branches=[
                            ExpressionBranchPayloadV2(
                                condition_groups=[
                                    ConditionGroupPayloadV2(
                                        conditions=[
                                            ConditionPayloadV2(
                                                operation="one_of",
                                                param_bindings=[
                                                    EngineParamBindingPayloadV2(
                                                        array_value=[
                                                            EngineParamBindingValuePayloadV2(
                                                                literal="SEV123",
                                                                reference="incident.severity",
                                                            )
                                                        ],
                                                        value=EngineParamBindingValuePayloadV2(
                                                            literal="SEV123",
                                                            reference="incident.severity",
                                                        ),
                                                    )
                                                ],
                                                subject="incident.severity",
                                            )
                                        ],
                                    )
                                ],
                                result=EngineParamBindingPayloadV2(
                                    array_value=[
                                        EngineParamBindingValuePayloadV2(
                                            literal="SEV123",
                                            reference="incident.severity",
                                        )
                                    ],
                                    value=EngineParamBindingValuePayloadV2(
                                        literal="SEV123",
                                        reference="incident.severity",
                                    ),
                                ),
                            )
                        ],
                        returns=ReturnsMetaV2(
                            array=True,
                            type="IncidentStatus",
                        ),
                    ),
                    concatenate=ExpressionConcatenateOptsPayloadV2(
                        reference='catalog_attribute["01FCNDV6P870EA6S7TK1DSYD5H"]',
                    ),
                    filter=ExpressionFilterOptsPayloadV2(
                        condition_groups=[
                            ConditionGroupPayloadV2(
                                conditions=[
                                    ConditionPayloadV2(
                                        operation="one_of",
                                        param_bindings=[
                                            EngineParamBindingPayloadV2(
                                                array_value=[
                                                    EngineParamBindingValuePayloadV2(
                                                        literal="SEV123",
                                                        reference="incident.severity",
                                                    )
                                                ],
                                                value=EngineParamBindingValuePayloadV2(
                                                    literal="SEV123",
                                                    reference="incident.severity",
                                                ),
                                            )
                                        ],
                                        subject="incident.severity",
                                    )
                                ],
                            )
                        ],
                    ),
                    navigate=ExpressionNavigateOptsPayloadV2(
                        reference='catalog_attribute["01FCNDV6P870EA6S7TK1DSYD5H"]',
                    ),
                    operation_type="navigate",
                    parse=ExpressionParseOptsPayloadV2(
                        returns=ReturnsMetaV2(
                            array=True,
                            type="IncidentStatus",
                        ),
                        source='metadata.annotations["github.com/repo"]',
                    ),
                )
            ],
            reference="abc123",
            root_reference="incident.status",
        )
    ],
    folder="My folder 01",
    include_private_escalations=True,
    include_private_incidents=True,
    name="My little workflow",
    once_for=["incident.url"],
    runs_on_incident_modes=["standard", "test", "retrospective"],
    runs_on_incidents="newly_created",
    shortform="page-the-ceo",
    state="active",
    steps=[
        StepConfigPayloadV2(
            for_each="abc123",
            id="abc123",
            name="pagerduty.escalate",
            param_bindings=[
                EngineParamBindingPayloadV2(
                    array_value=[
                        EngineParamBindingValuePayloadV2(
                            literal="SEV123",
                            reference="incident.severity",
                        )
                    ],
                    value=EngineParamBindingValuePayloadV2(
                        literal="SEV123",
                        reference="incident.severity",
                    ),
                )
            ],
        )
    ],
    trigger="incident.updated",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**condition_groups:** `typing.Sequence[ConditionGroupPayloadV2]` — Conditions that apply to the workflow trigger
    
</dd>
</dl>

<dl>
<dd>

**continue_on_step_error:** `bool` — Whether to continue executing the workflow if a step fails
    
</dd>
</dl>

<dl>
<dd>

**expressions:** `typing.Sequence[ExpressionPayloadV2]` — The expressions to use in the workflow
    
</dd>
</dl>

<dl>
<dd>

**include_private_incidents:** `bool` — Whether to include private incidents
    
</dd>
</dl>

<dl>
<dd>

**name:** `str` — Name provided by the user when creating the workflow
    
</dd>
</dl>

<dl>
<dd>

**once_for:** `typing.Sequence[str]` — This workflow will run 'once for' a list of references
    
</dd>
</dl>

<dl>
<dd>

**runs_on_incident_modes:** `typing.Sequence[WorkflowsCreateWorkflowPayloadV2RunsOnIncidentModesItem]` — Which incident modes should this workflow run on? By default, workflows only run on standard incidents, but can also be configured to run on test and retrospective incidents.
    
</dd>
</dl>

<dl>
<dd>

**runs_on_incidents:** `WorkflowsCreateWorkflowPayloadV2RunsOnIncidents` — Which incidents should the workflow be applied to?
    
</dd>
</dl>

<dl>
<dd>

**steps:** `typing.Sequence[StepConfigPayloadV2]` — Steps that are executed as part of the workflow
    
</dd>
</dl>

<dl>
<dd>

**trigger:** `str` — Trigger to set on the workflow
    
</dd>
</dl>

<dl>
<dd>

**annotations:** `typing.Optional[typing.Dict[str, str]]` — Annotations that track metadata about this resource
    
</dd>
</dl>

<dl>
<dd>

**delay:** `typing.Optional[WorkflowDelayV2]` 
    
</dd>
</dl>

<dl>
<dd>

**folder:** `typing.Optional[str]` — Folder to display the workflow in
    
</dd>
</dl>

<dl>
<dd>

**include_private_escalations:** `typing.Optional[bool]` — Whether to include private escalations
    
</dd>
</dl>

<dl>
<dd>

**shortform:** `typing.Optional[str]` — The shortform used to trigger this workflow (only applicable for manual triggers)
    
</dd>
</dl>

<dl>
<dd>

**state:** `typing.Optional[WorkflowsCreateWorkflowPayloadV2State]` — What state this workflow is in
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.workflows_v2.<a href="src/fern/workflows_v2/client.py">showworkflow</a>(...) -&gt; AsyncHttpResponse[WorkflowsShowWorkflowResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Show a workflow by ID
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.workflows_v2.showworkflow(
    id="01FCNDV6P870EA6S7TK1DSYDG0",
    skip_step_upgrades=False,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — Unique identifier for the workflow
    
</dd>
</dl>

<dl>
<dd>

**skip_step_upgrades:** `typing.Optional[bool]` — Skips workflow step upgrades, when the parameters for an existing workflow step change
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.workflows_v2.<a href="src/fern/workflows_v2/client.py">updateworkflow</a>(...) -&gt; AsyncHttpResponse[WorkflowsUpdateWorkflowResultV2]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Updates a workflow
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import (
    ConditionGroupPayloadV2,
    ConditionPayloadV2,
    EngineParamBindingPayloadV2,
    EngineParamBindingValuePayloadV2,
    ExpressionBranchesOptsPayloadV2,
    ExpressionBranchPayloadV2,
    ExpressionConcatenateOptsPayloadV2,
    ExpressionElseBranchPayloadV2,
    ExpressionFilterOptsPayloadV2,
    ExpressionNavigateOptsPayloadV2,
    ExpressionOperationPayloadV2,
    ExpressionParseOptsPayloadV2,
    ExpressionPayloadV2,
    IncidentIO,
    ReturnsMetaV2,
    StepConfigPayloadV2,
    WorkflowDelayV2,
)

client = IncidentIO()
client.workflows_v2.updateworkflow(
    id="01FCNDV6P870EA6S7TK1DSYDG0",
    annotations={"incident.io/terraform/version": "3.0.0"},
    condition_groups=[
        ConditionGroupPayloadV2(
            conditions=[
                ConditionPayloadV2(
                    operation="one_of",
                    param_bindings=[
                        EngineParamBindingPayloadV2(
                            array_value=[
                                EngineParamBindingValuePayloadV2(
                                    literal="SEV123",
                                    reference="incident.severity",
                                )
                            ],
                            value=EngineParamBindingValuePayloadV2(
                                literal="SEV123",
                                reference="incident.severity",
                            ),
                        )
                    ],
                    subject="incident.severity",
                )
            ],
        )
    ],
    continue_on_step_error=True,
    delay=WorkflowDelayV2(
        conditions_apply_over_delay=False,
        for_seconds=60,
    ),
    expressions=[
        ExpressionPayloadV2(
            else_branch=ExpressionElseBranchPayloadV2(
                result=EngineParamBindingPayloadV2(
                    array_value=[
                        EngineParamBindingValuePayloadV2(
                            literal="SEV123",
                            reference="incident.severity",
                        )
                    ],
                    value=EngineParamBindingValuePayloadV2(
                        literal="SEV123",
                        reference="incident.severity",
                    ),
                ),
            ),
            label="Team Slack channel",
            operations=[
                ExpressionOperationPayloadV2(
                    branches=ExpressionBranchesOptsPayloadV2(
                        branches=[
                            ExpressionBranchPayloadV2(
                                condition_groups=[
                                    ConditionGroupPayloadV2(
                                        conditions=[
                                            ConditionPayloadV2(
                                                operation="one_of",
                                                param_bindings=[
                                                    EngineParamBindingPayloadV2(
                                                        array_value=[
                                                            EngineParamBindingValuePayloadV2(
                                                                literal="SEV123",
                                                                reference="incident.severity",
                                                            )
                                                        ],
                                                        value=EngineParamBindingValuePayloadV2(
                                                            literal="SEV123",
                                                            reference="incident.severity",
                                                        ),
                                                    )
                                                ],
                                                subject="incident.severity",
                                            )
                                        ],
                                    )
                                ],
                                result=EngineParamBindingPayloadV2(
                                    array_value=[
                                        EngineParamBindingValuePayloadV2(
                                            literal="SEV123",
                                            reference="incident.severity",
                                        )
                                    ],
                                    value=EngineParamBindingValuePayloadV2(
                                        literal="SEV123",
                                        reference="incident.severity",
                                    ),
                                ),
                            )
                        ],
                        returns=ReturnsMetaV2(
                            array=True,
                            type="IncidentStatus",
                        ),
                    ),
                    concatenate=ExpressionConcatenateOptsPayloadV2(
                        reference='catalog_attribute["01FCNDV6P870EA6S7TK1DSYD5H"]',
                    ),
                    filter=ExpressionFilterOptsPayloadV2(
                        condition_groups=[
                            ConditionGroupPayloadV2(
                                conditions=[
                                    ConditionPayloadV2(
                                        operation="one_of",
                                        param_bindings=[
                                            EngineParamBindingPayloadV2(
                                                array_value=[
                                                    EngineParamBindingValuePayloadV2(
                                                        literal="SEV123",
                                                        reference="incident.severity",
                                                    )
                                                ],
                                                value=EngineParamBindingValuePayloadV2(
                                                    literal="SEV123",
                                                    reference="incident.severity",
                                                ),
                                            )
                                        ],
                                        subject="incident.severity",
                                    )
                                ],
                            )
                        ],
                    ),
                    navigate=ExpressionNavigateOptsPayloadV2(
                        reference='catalog_attribute["01FCNDV6P870EA6S7TK1DSYD5H"]',
                    ),
                    operation_type="navigate",
                    parse=ExpressionParseOptsPayloadV2(
                        returns=ReturnsMetaV2(
                            array=True,
                            type="IncidentStatus",
                        ),
                        source='metadata.annotations["github.com/repo"]',
                    ),
                )
            ],
            reference="abc123",
            root_reference="incident.status",
        )
    ],
    folder="My folder 01",
    include_private_escalations=True,
    include_private_incidents=True,
    name="My little workflow",
    once_for=["incident.url"],
    runs_on_incident_modes=["standard", "test", "retrospective"],
    runs_on_incidents="newly_created",
    shortform="page-the-ceo",
    state="active",
    steps=[
        StepConfigPayloadV2(
            for_each="abc123",
            id="abc123",
            name="pagerduty.escalate",
            param_bindings=[
                EngineParamBindingPayloadV2(
                    array_value=[
                        EngineParamBindingValuePayloadV2(
                            literal="SEV123",
                            reference="incident.severity",
                        )
                    ],
                    value=EngineParamBindingValuePayloadV2(
                        literal="SEV123",
                        reference="incident.severity",
                    ),
                )
            ],
        )
    ],
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — ID of the workflow to update
    
</dd>
</dl>

<dl>
<dd>

**condition_groups:** `typing.Sequence[ConditionGroupPayloadV2]` — Conditions that apply to the workflow trigger
    
</dd>
</dl>

<dl>
<dd>

**continue_on_step_error:** `bool` — Whether to continue executing the workflow if a step fails
    
</dd>
</dl>

<dl>
<dd>

**expressions:** `typing.Sequence[ExpressionPayloadV2]` — The expressions to use in the workflow
    
</dd>
</dl>

<dl>
<dd>

**include_private_incidents:** `bool` — Whether to include private incidents
    
</dd>
</dl>

<dl>
<dd>

**name:** `str` — Name provided by the user when creating the workflow
    
</dd>
</dl>

<dl>
<dd>

**once_for:** `typing.Sequence[str]` — This workflow will run 'once for' a list of references
    
</dd>
</dl>

<dl>
<dd>

**runs_on_incident_modes:** `typing.Sequence[WorkflowsUpdateWorkflowPayloadV2RunsOnIncidentModesItem]` — Which incident modes should this workflow run on? By default, workflows only run on standard incidents, but can also be configured to run on test and retrospective incidents.
    
</dd>
</dl>

<dl>
<dd>

**runs_on_incidents:** `WorkflowsUpdateWorkflowPayloadV2RunsOnIncidents` — Which incidents should the workflow be applied to?
    
</dd>
</dl>

<dl>
<dd>

**steps:** `typing.Sequence[StepConfigPayloadV2]` — Steps that are executed as part of the workflow
    
</dd>
</dl>

<dl>
<dd>

**annotations:** `typing.Optional[typing.Dict[str, str]]` — Annotations that track metadata about this resource
    
</dd>
</dl>

<dl>
<dd>

**delay:** `typing.Optional[WorkflowDelayV2]` 
    
</dd>
</dl>

<dl>
<dd>

**folder:** `typing.Optional[str]` — Folder to display the workflow in
    
</dd>
</dl>

<dl>
<dd>

**include_private_escalations:** `typing.Optional[bool]` — Whether to include private escalations
    
</dd>
</dl>

<dl>
<dd>

**shortform:** `typing.Optional[str]` — The shortform used to trigger this workflow (only applicable for manual triggers)
    
</dd>
</dl>

<dl>
<dd>

**state:** `typing.Optional[WorkflowsUpdateWorkflowPayloadV2State]` — What state this workflow is in
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.workflows_v2.<a href="src/fern/workflows_v2/client.py">destroyworkflow</a>(...) -&gt; AsyncHttpResponse[None]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Archives a workflow
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.workflows_v2.destroyworkflow(
    id="01FCNDV6P870EA6S7TK1DSYDG0",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — Unique identifier for the workflow
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Catalog V3
<details><summary><code>client.catalog_v3.<a href="src/fern/catalog_v3/client.py">listentries</a>(...) -&gt; AsyncHttpResponse[CatalogListEntriesResultV3]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List entries for a catalog type.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.catalog_v3.listentries(
    catalog_type_id="01FCNDV6P870EA6S7TK1DSYDG0",
    page_size=25,
    after="01FDAG4SAP5TYPT98WGR2N7W91",
    identifier="abc123",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**catalog_type_id:** `str` — ID of this catalog type
    
</dd>
</dl>

<dl>
<dd>

**page_size:** `int` — The integer number of records to return
    
</dd>
</dl>

<dl>
<dd>

**after:** `typing.Optional[str]` — An record's ID. This endpoint will return a list of records after this ID in relation to the API response order.
    
</dd>
</dl>

<dl>
<dd>

**identifier:** `typing.Optional[str]` 

If specified, only entries with this identifier will be returned. This will search by ID, external ID, and aliases.

If 'use name as identifier' is enabled for the catalog type, this will also match on name.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.catalog_v3.<a href="src/fern/catalog_v3/client.py">createentry</a>(...) -&gt; AsyncHttpResponse[CatalogCreateEntryResultV3]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create an entry within the catalog. We support a maximum of 50,000 entries per type.

If you call this API with a payload where the external_id and catalog_type_id match an existing entry, the existing entry will be updated.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import (
    CatalogEngineParamBindingPayloadV3,
    CatalogEngineParamBindingValuePayloadV3,
    IncidentIO,
)

client = IncidentIO()
client.catalog_v3.createentry(
    aliases=["lawrence@incident.io", "lawrence"],
    attribute_values={
        "abc123": CatalogEngineParamBindingPayloadV3(
            array_value=[
                CatalogEngineParamBindingValuePayloadV3(
                    literal="SEV123",
                )
            ],
            value=CatalogEngineParamBindingValuePayloadV3(
                literal="SEV123",
            ),
        )
    },
    catalog_type_id="01FCNDV6P870EA6S7TK1DSYDG0",
    external_id="761722cd-d1d7-477b-ac7e-90f9e079dc33",
    name="Primary On-call",
    rank=3,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**attribute_values:** `typing.Dict[str, CatalogEngineParamBindingPayloadV3]` — Values of this entry
    
</dd>
</dl>

<dl>
<dd>

**catalog_type_id:** `str` — ID of this catalog type
    
</dd>
</dl>

<dl>
<dd>

**name:** `str` — Name is the human readable name of this entry
    
</dd>
</dl>

<dl>
<dd>

**aliases:** `typing.Optional[typing.Sequence[str]]` — Optional aliases that can be used to reference this entry
    
</dd>
</dl>

<dl>
<dd>

**external_id:** `typing.Optional[str]` — An optional alternative ID for this entry, which is ensured to be unique for the type
    
</dd>
</dl>

<dl>
<dd>

**rank:** `typing.Optional[int]` — When catalog type is ranked, this is used to help order things
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.catalog_v3.<a href="src/fern/catalog_v3/client.py">bulkupdateentries</a>(...) -&gt; AsyncHttpResponse[None]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update multiple catalog entries in a single operation. You can update up to 250 entries at once. This operation is atomic - either all entries are updated successfully, or none are updated.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import (
    CatalogEngineParamBindingPayloadV3,
    CatalogEngineParamBindingValuePayloadV3,
    IncidentIO,
    PartialEntryPayloadV3,
)

client = IncidentIO()
client.catalog_v3.bulkupdateentries(
    catalog_type_id="01GW2G3V0S59R238FAHPDS1R66",
    entries=[
        PartialEntryPayloadV3(
            aliases=["abc123"],
            attribute_values={
                "abc123": CatalogEngineParamBindingPayloadV3(
                    array_value=[
                        CatalogEngineParamBindingValuePayloadV3(
                            literal="SEV123",
                        )
                    ],
                    value=CatalogEngineParamBindingValuePayloadV3(
                        literal="SEV123",
                    ),
                )
            },
            entry_id="abc123",
            external_id="abc123",
            name="abc123",
            rank=1,
        ),
        PartialEntryPayloadV3(
            aliases=["abc123"],
            attribute_values={
                "abc123": CatalogEngineParamBindingPayloadV3(
                    array_value=[
                        CatalogEngineParamBindingValuePayloadV3(
                            literal="SEV123",
                        )
                    ],
                    value=CatalogEngineParamBindingValuePayloadV3(
                        literal="SEV123",
                    ),
                )
            },
            entry_id="abc123",
            external_id="abc123",
            name="abc123",
            rank=1,
        ),
    ],
    update_attributes=[
        "01GW2G3V0S59R238FAHPDS1R66",
        "01GW2G3V0S59R238FAHPDS1R67",
    ],
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**catalog_type_id:** `str` — The unique identifier of the catalog type containing the entries
    
</dd>
</dl>

<dl>
<dd>

**entries:** `typing.Sequence[PartialEntryPayloadV3]` — A list of entries to update with their new values. Maximum 250 entries per request.
    
</dd>
</dl>

<dl>
<dd>

**update_attributes:** `typing.Optional[typing.Sequence[str]]` — Optional list of specific attribute IDs to update across all entries. When provided, only these attributes in attribute_values will be updated and all other attributes will be preserved. This parameter only affects attribute_values - it does not affect core entry fields like name, rank, aliases, or external_id, which follow their individual omission rules.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.catalog_v3.<a href="src/fern/catalog_v3/client.py">showentry</a>(...) -&gt; AsyncHttpResponse[CatalogShowEntryResultV3]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Show a single catalog entry.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.catalog_v3.showentry(
    id="01FCNDV6P870EA6S7TK1DSYDG0",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — ID of this catalog entry
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.catalog_v3.<a href="src/fern/catalog_v3/client.py">updateentry</a>(...) -&gt; AsyncHttpResponse[CatalogUpdateEntryResultV3]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Updates an existing catalog entry.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import (
    CatalogEngineParamBindingPayloadV3,
    CatalogEngineParamBindingValuePayloadV3,
    IncidentIO,
)

client = IncidentIO()
client.catalog_v3.updateentry(
    id="01FCNDV6P870EA6S7TK1DSYDG0",
    aliases=["lawrence@incident.io", "lawrence"],
    attribute_values={
        "abc123": CatalogEngineParamBindingPayloadV3(
            array_value=[
                CatalogEngineParamBindingValuePayloadV3(
                    literal="SEV123",
                )
            ],
            value=CatalogEngineParamBindingValuePayloadV3(
                literal="SEV123",
            ),
        )
    },
    external_id="761722cd-d1d7-477b-ac7e-90f9e079dc33",
    name="Primary On-call",
    rank=3,
    update_attributes=["abc123"],
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — ID of this catalog entry
    
</dd>
</dl>

<dl>
<dd>

**attribute_values:** `typing.Dict[str, CatalogEngineParamBindingPayloadV3]` — Values of this entry
    
</dd>
</dl>

<dl>
<dd>

**name:** `str` — Name is the human readable name of this entry
    
</dd>
</dl>

<dl>
<dd>

**aliases:** `typing.Optional[typing.Sequence[str]]` — Optional aliases that can be used to reference this entry
    
</dd>
</dl>

<dl>
<dd>

**external_id:** `typing.Optional[str]` — An optional alternative ID for this entry, which is ensured to be unique for the type
    
</dd>
</dl>

<dl>
<dd>

**rank:** `typing.Optional[int]` — When catalog type is ranked, this is used to help order things
    
</dd>
</dl>

<dl>
<dd>

**update_attributes:** `typing.Optional[typing.Sequence[str]]` 

If provided, only update these attribute_values keys. If not provided, update all attribute values.
If you specify an attribute key that's not in your payload, the associated attribute value will be cleared.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.catalog_v3.<a href="src/fern/catalog_v3/client.py">destroyentry</a>(...) -&gt; AsyncHttpResponse[None]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Archives a catalog entry.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.catalog_v3.destroyentry(
    id="01FCNDV6P870EA6S7TK1DSYDG0",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — ID of this catalog entry
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.catalog_v3.<a href="src/fern/catalog_v3/client.py">listresources</a>() -&gt; AsyncHttpResponse[CatalogListResourcesResultV3]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List available engine resources for the catalog.

A resource represents a type of data that can be held within the catalog, so this
endpoint can be used to see what attribute types can be used when updating the
schema of a catalog type.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.catalog_v3.listresources()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.catalog_v3.<a href="src/fern/catalog_v3/client.py">listtypes</a>() -&gt; AsyncHttpResponse[CatalogListTypesResultV3]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List all catalog types for an organisation, including those synced from external resources.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.catalog_v3.listtypes()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.catalog_v3.<a href="src/fern/catalog_v3/client.py">createtype</a>(...) -&gt; AsyncHttpResponse[CatalogCreateTypeResultV3]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a catalog type. The schema must be updated using the UpdateTypeSchema endpoint.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.catalog_v3.createtype(
    annotations={"incident.io/catalog-importer/id": "id-of-config"},
    categories=["customer"],
    color="yellow",
    description="Represents Kubernetes clusters that we run inside of GKE.",
    icon="alert",
    name="Kubernetes Cluster",
    ranked=True,
    source_repo_url="https://github.com/my-company/incident-io-catalog",
    type_name='Custom["BackstageGroup"]',
    use_name_as_identifier=True,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**description:** `str` — Human readble description of this type
    
</dd>
</dl>

<dl>
<dd>

**name:** `str` — Name is the human readable name of this type
    
</dd>
</dl>

<dl>
<dd>

**annotations:** `typing.Optional[typing.Dict[str, str]]` — Annotations that can track metadata about this type
    
</dd>
</dl>

<dl>
<dd>

**categories:** `typing.Optional[typing.Sequence[CatalogCreateTypePayloadV3CategoriesItem]]` — What categories is this type considered part of
    
</dd>
</dl>

<dl>
<dd>

**color:** `typing.Optional[CatalogCreateTypePayloadV3Color]` — Sets the display color of this type in the dashboard
    
</dd>
</dl>

<dl>
<dd>

**icon:** `typing.Optional[CatalogCreateTypePayloadV3Icon]` — Sets the display icon of this type in the dashboard
    
</dd>
</dl>

<dl>
<dd>

**ranked:** `typing.Optional[bool]` — If this type should be ranked
    
</dd>
</dl>

<dl>
<dd>

**source_repo_url:** `typing.Optional[str]` — The url of the external repository where this type is managed
    
</dd>
</dl>

<dl>
<dd>

**type_name:** `typing.Optional[str]` — The type name of this catalog type, to be used when defining attributes. This is immutable once a CatalogType has been created. For non-externally sync types, it must follow the pattern Custom["SomeName"]
    
</dd>
</dl>

<dl>
<dd>

**use_name_as_identifier:** `typing.Optional[bool]` — If enabled, you can refer to entries of this type by their name, as well as their external ID and any aliases.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.catalog_v3.<a href="src/fern/catalog_v3/client.py">showtype</a>(...) -&gt; AsyncHttpResponse[CatalogShowTypeResultV3]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Show a single catalog type.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.catalog_v3.showtype(
    id="01FCNDV6P870EA6S7TK1DSYDG0",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — ID of this catalog type
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.catalog_v3.<a href="src/fern/catalog_v3/client.py">updatetype</a>(...) -&gt; AsyncHttpResponse[CatalogUpdateTypeResultV3]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Updates an existing catalog type. The schema must be updated using the UpdateTypeSchema endpoint.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.catalog_v3.updatetype(
    id="01FCNDV6P870EA6S7TK1DSYDG0",
    annotations={"incident.io/catalog-importer/id": "id-of-config"},
    categories=["customer"],
    color="yellow",
    description="Represents Kubernetes clusters that we run inside of GKE.",
    icon="alert",
    name="Kubernetes Cluster",
    ranked=True,
    source_repo_url="https://github.com/my-company/incident-io-catalog",
    use_name_as_identifier=True,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — ID of this catalog type
    
</dd>
</dl>

<dl>
<dd>

**description:** `str` — Human readble description of this type
    
</dd>
</dl>

<dl>
<dd>

**name:** `str` — Name is the human readable name of this type
    
</dd>
</dl>

<dl>
<dd>

**annotations:** `typing.Optional[typing.Dict[str, str]]` — Annotations that can track metadata about this type
    
</dd>
</dl>

<dl>
<dd>

**categories:** `typing.Optional[typing.Sequence[CatalogUpdateTypePayloadV3CategoriesItem]]` — What categories is this type considered part of
    
</dd>
</dl>

<dl>
<dd>

**color:** `typing.Optional[CatalogUpdateTypePayloadV3Color]` — Sets the display color of this type in the dashboard
    
</dd>
</dl>

<dl>
<dd>

**icon:** `typing.Optional[CatalogUpdateTypePayloadV3Icon]` — Sets the display icon of this type in the dashboard
    
</dd>
</dl>

<dl>
<dd>

**ranked:** `typing.Optional[bool]` — If this type should be ranked
    
</dd>
</dl>

<dl>
<dd>

**source_repo_url:** `typing.Optional[str]` — The url of the external repository where this type is managed
    
</dd>
</dl>

<dl>
<dd>

**use_name_as_identifier:** `typing.Optional[bool]` — If enabled, you can refer to entries of this type by their name, as well as their external ID and any aliases.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.catalog_v3.<a href="src/fern/catalog_v3/client.py">destroytype</a>(...) -&gt; AsyncHttpResponse[None]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Archives a catalog type and associated entries.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import IncidentIO

client = IncidentIO()
client.catalog_v3.destroytype(
    id="01FCNDV6P870EA6S7TK1DSYDG0",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — ID of this catalog type
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.catalog_v3.<a href="src/fern/catalog_v3/client.py">updatetypeschema</a>(...) -&gt; AsyncHttpResponse[CatalogUpdateTypeSchemaResultV3]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update an existing catalog types schema, adding or removing attributes.

Updating the schema is handled separately from creating and updating types, so that you don't
have to worry about dependencies between types. For example, if type A has an attribute that
relies on type B, you would have to create type B first.

By allowing the creation of types without a schema, they can be created in any order, but it
means that you need to make a separate call to this endpoint to update the schema.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from fern import (
    CatalogTypeAttributePathItemPayloadV3,
    CatalogTypeAttributePayloadV3,
    IncidentIO,
)

client = IncidentIO()
client.catalog_v3.updatetypeschema(
    id="01FCNDV6P870EA6S7TK1DSYDG0",
    attributes=[
        CatalogTypeAttributePayloadV3(
            array=False,
            backlink_attribute="abc123",
            id="01GW2G3V0S59R238FAHPDS1R66",
            mode="",
            name="tier",
            path=[
                CatalogTypeAttributePathItemPayloadV3(
                    attribute_id="abc123",
                )
            ],
            type='Custom["Service"]',
        )
    ],
    version=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` — ID of this catalog type
    
</dd>
</dl>

<dl>
<dd>

**attributes:** `typing.Sequence[CatalogTypeAttributePayloadV3]` 
    
</dd>
</dl>

<dl>
<dd>

**version:** `int` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

