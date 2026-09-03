---
title: Data Storage Mechanism for Manifested Containers Updated
author: Millie Deiry
hidden: true
published_at: '2024-08-07T13:07:24.981Z'
type: improved
---
The information about manifested containers is now stored in the database for future reference. A new field called ‘Container Status’ has been added to all the relevant Container APIs to store and retrieve the container information based on status. The ‘Container Status’ can either be ‘Active’ or ‘Manifested’. Customers can only add or remove shipments from containers with an ‘Active’ status. Containers can only be manifested if they have an ‘Active’ status. Containers in the ‘Manifested’ status cannot be deleted. 

For example, in the Get Containers API, the query parameters in the API request have been updated to include the optional parameter 'containerStatus,' and the API response now includes the containerStatus field populated with the container's status, either 'Active' or 'Manifested'. For more information on managing shipments in a container, please refer to the API reference page and the Sapient Core API section.