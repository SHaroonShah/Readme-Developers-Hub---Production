---
title: New API – Delete Shipping Location
author: Intersoft
hidden: true
published_at: '2023-05-11T12:31:13.305Z'
type: added
---
A new Delete API service has been added to the Shipping Locations API – see the API Reference section for full details of this new API. This allows an existing shipping location to be deleted. It will not be possible to delete a shipping location that is linked to one or more shipping accounts or user accounts; in this scenario the shipping location will need to be un-linked from the shipping account/user account via either the API or UI before it can be deleted. In all other scenarios it will be possible to delete the shipping location.