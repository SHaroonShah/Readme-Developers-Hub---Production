---
title: Pagination bar
excerpt: >-
  Some tables in SAPIENT may have more content that can be displayed on one
  page. Use the paginatioin bar at the bottom of the contents panel view more of
  the current table items.
deprecated: false
hidden: false
icon: fad fa-input-numeric
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---

<Image src="https://files.readme.io/22ae167a5c65b3b4feed20f0922d1a08b0eaca9c647ac0b74eb2b9ef89debe35-Pagination_bar.png" alt="Pagination bar" align="center" caption="SAPIENT pagination bar" border={true} />


Refer to the following table to find out more about the pagination bar options.

|                                                 Element                                                 | Description                                                                         |
| :-----------------------------------------------------------------------------------------------------: | :---------------------------------------------------------------------------------- |
| ![](https://files.readme.io/634a00bc841cf01628832d5a4aad89ca063bb66fd937c82c203ea2ff35983772-image.png) | Select it to go back to the previous page of the table.                             |
| ![](https://files.readme.io/f5cb653d6e09610464ab366d78f014a8fdebdb7650ab6c44fe67b1147b6d3b1a-image.png) | Select it to go to the next page of the table.                                      |
| ![](https://files.readme.io/b80a36d5afe2a630610ac19b3fe0a6028c263b2a941fa9a9b8efb1ca49af8faf-image.png) | Select the desired page number that you want to view in the table.                  |
| ![](https://files.readme.io/4864d2edc0b5afcd2b947902b806c09a9bf417d8c1672c36554fe3e5c064ce7b-image.png) | Represents the number of items currently displayed and the total number in a table. |

<Callout icon="💡" theme="default">
  ### _Tip_

  _You can also limit the number of entities in the table by selecting the entities from the&#x20;_**_entries per page_**_&#x20;&#x20;_![alt text](https://files.readme.io/9d9c6f5d79965d90b05c5d1826fb9c162f6733773a1962135047bb0c633710aa-Prev_button.png)_&#x20;dropdown._
</Callout>



<AdvancedTable
  data={[
    {
      'code': 'APIKEY_EMPTY',
      'status': 'Unauthorized',
      'description': 'An API key was not supplied.',
      'message': 'You must pass in an API key.'
    },
    {
      'code': 'APIKEY_MISMATCH',
      'status': 'Forbidden',
      'description': "The API key doesn't match the project.",
      'message': "The API key doesn't match the project."
    },
    {
      'code': 'APIKEY_NOTFOUND',
      'status': 'Unauthorized',
      'description': "The API key couldn't be located.",
      'message': "We couldn't find your API key."
    },
    {
      'code': 'API_ACCESS_REVOKED',
      'status': 'Forbidden',
      'description': 'Your ReadMe API access has been revoked.',
      'message': 'Your ReadMe API access has been revoked.'
    },
    {
      'code': 'API_ACCESS_UNAVAILABLE',
      'status': 'Forbidden',
      'description': 'Your ReadMe project does not have access to this API. Please reach out to support@readme.io.',
      'message': 'Your ReadMe project does not have access to this API. Please reach out to support@readme.io.'
    },
    {
      'code': 'APPLY_INVALID_EMAIL',
      'status': 'Bad Request',
      'description': 'You need to provide a valid email.',
      'message': 'You need to provide a valid email.'
    },
    {
      'code': 'APPLY_INVALID_JOB',
      'status': 'Bad Request',
      'description': 'You need to provide a job.',
      'message': 'You need to provide a job.'
    },
    {
      'code': 'APPLY_INVALID_NAME',
      'status': 'Bad Request',
      'description': 'You need to provide a name.',
      'message': 'You need to provide a name.'
    },
    {
      'code': 'CATEGORY_INVALID',
      'status': 'Bad Request',
      'description': "The category couldn't be saved.",
      'message': "We couldn't save this category ({error})."
    },
    {
      'code': 'CATEGORY_NOTFOUND',
      'status': 'Not Found',
      'description': "The category couldn't be found.",
      'message': "The category with the slug '{category}' couldn't be found."
    },
    {
      'code': 'CHANGELOG_INVALID',
      'status': 'Bad Request',
      'description': "The changelog couldn't be saved.",
      'message': "We couldn't save this changelog ({error})."
    },
    {
      'code': 'CHANGELOG_NOTFOUND',
      'status': 'Not Found',
      'description': "The changelog couldn't be found.",
      'message': "The changelog with the slug '{slug}' couldn't be found."
    }
  ]}
/>
