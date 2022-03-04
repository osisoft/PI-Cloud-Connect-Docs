---
uid: define-publication-scope
---

# Define publication scope

The Publication Scope step allows you to select either the publication type of AF Elements or of AF Templates for publication. AF Element Publications include the selected AF Element, all Child Elements, all templates referenced by the elements included, all attributes, and all data references. Only include AF Elements with [Supported AF objects](xref:supported-af-objects) in AF Element Publications. For users who only need to publish templates AF Template Publications will include all AF Templates contained within the `AFServer.AFDatabase` namespace selected in the previous step.

**Note:** AF Element publications include referenced AF Templates, and it is not necessary to create both an AF Element publication and AF Template publication in order to publish templates.

## Procedure

1. Select **AF Element** or **AF Templates** from the dropdown menu.

1. For **AF Element** publications select the AF element that you want to publish.

1. For **AF Template** publications the wizard will go directly to the Publication Name step.

1. Click the **arrow button** at the bottom of the screen.
