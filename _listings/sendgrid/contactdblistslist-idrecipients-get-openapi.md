---
swagger: "2.0"
x-collection-name: SendGrid
x-complete: 0
info:
  title: SendGrid Get Contactdb Lists List  Recipients
  description: "**This endpoint allows you to retrieve all recipients on the list
    with the given ID.** \n\nThe Contacts API helps you manage your [Marketing Campaigns](https://sendgrid.com/docs/User_Guide/Marketing_Campaigns/index.html)
    recipients."
  version: 1.0.0
host: api.sendgrid.com
basePath: /v3
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /access_settings/activity:
    get:
      summary: Get Access Settings Activity
      description: |-
        **This endpoint allows you to retrieve a list of all of the IP addresses that recently attempted to access your account either through the User Interface or the API.**

        IP Access Management allows you to control which IP addresses can be used to access your account, either through the User Interface or the API. There is no limit to the number of IP addresses that you can add to your whitelist. It is possible to remove your own IP address from the whitelist, thus preventing yourself from accessing your account.

        For more information, please see our [User Guide](http://sendgrid.com/docs/User_Guide/Settings/ip_access_management.html).
      operationId: access_settings.activity.get
      x-api-path-slug: access-settingsactivity-get
      parameters:
      - in: query
        name: limit
        description: Limits the number of IPs to return
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Access
      - Settings
      - Activity
  /access_settings/whitelist:
    delete:
      summary: Delete Access Settings Whitelist
      description: |-
        **This endpoint allows you to remove one or more IPs from your IP whitelist.**

        You can remove one IP at a time, or you can remove multiple IP addresses.

        IP Access Management allows you to control which IP addresses can be used to access your account, either through the User Interface or the API. There is no limit to the number of IP addresses that you can add to your whitelist. It is possible to remove your own IP address from the whitelist, thus preventing yourself from accessing your account.

        For more information, please see our [User Guide](http://sendgrid.com/docs/User_Guide/Settings/ip_access_management.html).
      operationId: access_settings.whitelist.delete
      x-api-path-slug: access-settingswhitelist-delete
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Access
      - Settings
      - Whitelist
    get:
      summary: Get Access Settings Whitelist
      description: |-
        **This endpoint allows you to retrieve a list of IP addresses that are currently whitelisted.**

        IP Access Management allows you to control which IP addresses can be used to access your account, either through the User Interface or the API. There is no limit to the number of IP addresses that you can add to your whitelist. It is possible to remove your own IP address from the whitelist, thus preventing yourself from accessing your account.

        For more information, please see our [User Guide](http://sendgrid.com/docs/User_Guide/Settings/ip_access_management.html).
      operationId: access_settings.whitelist.get
      x-api-path-slug: access-settingswhitelist-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Access
      - Settings
      - Whitelist
    post:
      summary: Add Access Settings Whitelist
      description: |-
        **This endpoint allows you to add one or more IP addresses to your IP whitelist.**

        When adding an IP to your whitelist, include the IP address in an array. You can whitelist one IP at a time, or you can whitelist multiple IPs at once.

        IP Access Management allows you to control which IP addresses can be used to access your account, either through the User Interface or the API. There is no limit to the number of IP addresses that you can add to your whitelist. It is possible to remove your own IP address from the whitelist, thus preventing yourself from accessing your account.

        For more information, please see our [User Guide](http://sendgrid.com/docs/User_Guide/Settings/ip_access_management.html).
      operationId: access_settings.whitelist.post
      x-api-path-slug: access-settingswhitelist-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Access
      - Settings
      - Whitelist
  /access_settings/whitelist/{rule_id}:
    delete:
      summary: Delete Access Settings Whitelist Rule
      description: |-
        **This endpoint allows you to remove a specific IP address from your IP whitelist.**

        When removing a specific IP address from your whitelist, you must include the ID in your call.

        IP Access Management allows you to control which IP addresses can be used to access your account, either through the User Interface or the API. There is no limit to the number of IP addresses that you can add to your whitelist. It is possible to remove your own IP address from the whitelist, thus preventing yourself from accessing your account.

        For more information, please see our [User Guide](http://sendgrid.com/docs/User_Guide/Settings/ip_access_management.html).
      operationId: access_settings.whitelist.rule_id.delete
      x-api-path-slug: access-settingswhitelistrule-id-delete
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Access
      - Settings
      - Whitelist
      - Rule
    get:
      summary: Get Access Settings Whitelist Rule
      description: |-
        **This endpoint allows you to retreive a specific IP address that has been whitelisted.**

        You must include the ID for the specific IP address you want to retrieve in your call.

        IP Access Management allows you to control which IP addresses can be used to access your account, either through the User Interface or the API. There is no limit to the number of IP addresses that you can add to your whitelist. It is possible to remove your own IP address from the whitelist, thus preventing yourself from accessing your account.

        For more information, please see our [User Guide](http://sendgrid.com/docs/User_Guide/Settings/ip_access_management.html).
      operationId: access_settings.whitelist.rule_id.get
      x-api-path-slug: access-settingswhitelistrule-id-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Access
      - Settings
      - Whitelist
      - Rule
  /alerts:
    get:
      summary: Get Alerts
      description: "**This endpoint allows you to retieve all of your alerts.**\n\nAlerts
        allow you to specify an email address to receive notifications regarding your
        email usage or statistics. \n* Usage alerts allow you to set the threshold
        at which an alert will be sent.\n* Stats notifications allow you to set how
        frequently you would like to receive email statistics reports. For example,
        \"daily\", \"weekly\", or \"monthly\".\n\nFor more information about alerts,
        please see our [User Guide](https://sendgrid.com/docs/User_Guide/Settings/alerts.html)."
      operationId: GET_alerts
      x-api-path-slug: alerts-get
      parameters:
      - in: header
        name: Authorization
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Alerts
    post:
      summary: Add Alerts
      description: |-
        **This endpoint allows you to create a new alert.**

        Alerts allow you to specify an email address to receive notifications regarding your email usage or statistics. There are two types of alerts that can be created with this endpoint:

        * `usage_limit` allows you to set the threshold at which an alert will be sent.
        * `stats_notification` allows you to set how frequently you would like to receive email statistics reports. For example, "daily", "weekly", or "monthly".

        For more information about alerts, please see our [User Guide](https://sendgrid.com/docs/User_Guide/Settings/alerts.html).
      operationId: POST_alerts
      x-api-path-slug: alerts-post
      parameters:
      - in: header
        name: Authorization
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: on-behalf-of
      responses:
        200:
          description: OK
      tags:
      - Email
      - Alerts
  /alerts/{alert_id}:
    delete:
      summary: Delete Alerts Alert
      description: "**This endpoint allows you to delete an alert.**\n\nAlerts allow
        you to specify an email address to receive notifications regarding your email
        usage or statistics. \n* Usage alerts allow you to set the threshold at which
        an alert will be sent.\n* Stats notifications allow you to set how frequently
        you would like to receive email statistics reports. For example, \"daily\",
        \"weekly\", or \"monthly\".\n\nFor more information about alerts, please see
        our [User Guide](https://sendgrid.com/docs/User_Guide/Settings/alerts.html)."
      operationId: alerts.alert_id.delete
      x-api-path-slug: alertsalert-id-delete
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Alerts
      - Alert
    get:
      summary: Get Alerts Alert
      description: "**This endpoint allows you to retrieve a specific alert.**\n\nAlerts
        allow you to specify an email address to receive notifications regarding your
        email usage or statistics. \n* Usage alerts allow you to set the threshold
        at which an alert will be sent.\n* Stats notifications allow you to set how
        frequently you would like to receive email statistics reports. For example,
        \"daily\", \"weekly\", or \"monthly\".\n\nFor more information about alerts,
        please see our [User Guide](https://sendgrid.com/docs/User_Guide/Settings/alerts.html)."
      operationId: alerts.alert_id.get
      x-api-path-slug: alertsalert-id-get
      parameters:
      - in: header
        name: Authorization
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Alerts
      - Alert
    patch:
      summary: Patch Alerts Alert
      description: "**This endpoint allows you to update an alert.**\n\nAlerts allow
        you to specify an email address to receive notifications regarding your email
        usage or statistics. \n* Usage alerts allow you to set the threshold at which
        an alert will be sent.\n* Stats notifications allow you to set how frequently
        you would like to receive email statistics reports. For example, \"daily\",
        \"weekly\", or \"monthly\".\n\nFor more information about alerts, please see
        our [User Guide](https://sendgrid.com/docs/User_Guide/Settings/alerts.html)."
      operationId: alerts.alert_id.patch
      x-api-path-slug: alertsalert-id-patch
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Alerts
      - Alert
  /api_keys:
    get:
      summary: Get Api Keys
      description: |-
        **This endpoint allows you to retrieve all API Keys that belong to the authenticated user.**

        The API Keys feature allows customers to be able to generate an API Key credential which can be used for authentication with the SendGrid v3 Web API or the [Mail API Endpoint](https://sendgrid.com/docs/API_Reference/Web_API/mail.html).
      operationId: GET_api_keys
      x-api-path-slug: api-keys-get
      parameters:
      - in: query
        name: limit
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Api
      - Keys
    post:
      summary: Add Api Keys
      description: |-
        **This endpoint allows you to create a new random API Key for the user.**

        A JSON request body containing a "name" property is required. If number of maximum keys is reached, HTTP 403 will be returned.

        There is a limit of 100 API Keys on your account.

        The API Keys feature allows customers to be able to generate an API Key credential which can be used for authentication with the SendGrid v3 Web API or the [Mail API Endpoint](https://sendgrid.com/docs/API_Reference/Web_API/mail.html).

        See the [API Key Permissions List](https://sendgrid.com/docs/API_Reference/Web_API_v3/API_Keys/api_key_permissions_list.html) for a list of all available scopes.
      operationId: api_keys.post
      x-api-path-slug: api-keys-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Api
      - Keys
  /api_keys/{api_key_id}:
    delete:
      summary: Delete Api Keys Api Key
      description: |-
        **This endpoint allows you to revoke an existing API Key**

        Authentications using this API Key will fail after this request is made, with some small propogation delay.If the API Key ID does not exist an HTTP 404 will be returned.

        The API Keys feature allows customers to be able to generate an API Key credential which can be used for authentication with the SendGrid v3 Web API or the [Mail API Endpoint](https://sendgrid.com/docs/API_Reference/Web_API/mail.html).

        ## URI Parameters

        | URI Parameter   | Type  | Required?  | Description  |
        |---|---|---|---|
        |api_key_id |string | required | The ID of the API Key you are deleting.|
      operationId: api_keys.api_key_id.delete
      x-api-path-slug: api-keysapi-key-id-delete
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Api
      - Keys
      - Api
      - Key
    get:
      summary: Get Api Keys Api Key
      description: |-
        **This endpoint allows you to retrieve a single api key.**

        If the API Key ID does not exist an HTTP 404 will be returned.
      operationId: api_keys.api_key_id.get
      x-api-path-slug: api-keysapi-key-id-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Api
      - Keys
      - Api
      - Key
    patch:
      summary: Patch Api Keys Api Key
      description: |-
        **This endpoint allows you to update the name of an existing API Key.**

        A JSON request body with a "name" property is required.

        The API Keys feature allows customers to be able to generate an API Key credential which can be used for authentication with the SendGrid v3 Web API or the [Mail API Endpoint](https://sendgrid.com/docs/API_Reference/Web_API/mail.html).

        ## URI Parameters

        | URI Parameter   | Type  | Required?  | Description  |
        |---|---|---|---|
        |api_key_id |string | required | The ID of the API Key you are updating.|
      operationId: api_keys.api_key_id.patch
      x-api-path-slug: api-keysapi-key-id-patch
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Api
      - Keys
      - Api
      - Key
    put:
      summary: Put Api Keys Api Key
      description: |-
        **This endpoint allows you to update the name and scopes of a given API key.**

        A JSON request body with a "name" property is required.
        Most provide the list of all the scopes an api key should have.

        The API Keys feature allows customers to be able to generate an API Key credential which can be used for authentication with the SendGrid v3 Web API or the [Mail API Endpoint](https://sendgrid.com/docs/API_Reference/Web_API/mail.html).
      operationId: api_keys.api_key_id.put
      x-api-path-slug: api-keysapi-key-id-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Api
      - Keys
      - Api
      - Key
  /asm/groups:
    get:
      summary: Get Asm Groups
      description: |-
        **This endpoint allows you to retrieve information about multiple suppression groups.**

        This endpoint will return information for each group ID that you include in your request. To add a group ID to your request, simply append `&id=` followed by the group ID.

        Suppressions are a list of email addresses that will not receive content sent under a given [group](https://sendgrid.com/docs/API_Reference/Web_API_v3/Suppression_Management/groups.html).

        Suppression groups, or [unsubscribe groups](https://sendgrid.com/docs/API_Reference/Web_API_v3/Suppression_Management/groups.html), allow you to label a category of content that you regularly send. This gives your recipients the ability to opt out of a specific set of your email. For example, you might define a group for your transactional email, and one for your marketing email so that your users can continue recieving your transactional email witout having to receive your marketing content.
      operationId: asm.groups.get
      x-api-path-slug: asmgroups-get
      parameters:
      - in: query
        name: id
        description: The ID of a suppression group that you want to retrieve information
          for
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Asm
      - Groups
    post:
      summary: Add Asm Groups
      description: |-
        **This endpoint allows you to create a new suppression group.**

        Suppression groups, or unsubscribe groups, are specific types or categories of email that you would like your recipients to be able to unsubscribe from. For example: Daily Newsletters, Invoices, System Alerts.

        The **name** and **description** of the unsubscribe group will be visible by recipients when they are managing their subscriptions.

        Each user can create up to 25 different suppression groups.
      operationId: asm.groups.post
      x-api-path-slug: asmgroups-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Asm
      - Groups
  /asm/groups/{group_id}:
    delete:
      summary: Delete Asm Groups Group
      description: |-
        **This endpoint allows you to delete a suppression group.**

        You can only delete groups that have not been attached to sent mail in the last 60 days. If a recipient uses the "one-click unsubscribe" option on an email associated with a deleted group, that recipient will be added to the global suppression list.

        Suppression groups, or unsubscribe groups, are specific types or categories of email that you would like your recipients to be able to unsubscribe from. For example: Daily Newsletters, Invoices, System Alerts.

        The **name** and **description** of the unsubscribe group will be visible by recipients when they are managing their subscriptions.

        Each user can create up to 25 different suppression groups.
      operationId: asm.groups.group_id.delete
      x-api-path-slug: asmgroupsgroup-id-delete
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Asm
      - Groups
      - Group
    get:
      summary: Get Asm Groups Group
      description: |-
        **This endpoint allows you to retrieve a single suppression group.**

        Suppression groups, or unsubscribe groups, are specific types or categories of email that you would like your recipients to be able to unsubscribe from. For example: Daily Newsletters, Invoices, System Alerts.

        The **name** and **description** of the unsubscribe group will be visible by recipients when they are managing their subscriptions.

        Each user can create up to 25 different suppression groups.
      operationId: asm.groups.group_id.get
      x-api-path-slug: asmgroupsgroup-id-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Asm
      - Groups
      - Group
    patch:
      summary: Patch Asm Groups Group
      description: |-
        **This endpoint allows you to update or change a suppression group.**

        Suppression groups, or unsubscribe groups, are specific types or categories of email that you would like your recipients to be able to unsubscribe from. For example: Daily Newsletters, Invoices, System Alerts.

        The **name** and **description** of the unsubscribe group will be visible by recipients when they are managing their subscriptions.

        Each user can create up to 25 different suppression groups.
      operationId: asm.groups.group_id.patch
      x-api-path-slug: asmgroupsgroup-id-patch
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Asm
      - Groups
      - Group
  /asm/groups/{group_id}/suppressions:
    get:
      summary: Get Asm Groups Group  Suppressions
      description: |-
        **This endpoint allows you to retrieve all suppressed email addresses belonging to the given group.**

        Suppressions are recipient email addresses that are added to [unsubscribe groups](https://sendgrid.com/docs/API_Reference/Web_API_v3/Suppression_Management/groups.html). Once a recipient's address is on the suppressions list for an unsubscribe group, they will not receive any emails that are tagged with that unsubscribe group.
      operationId: asm.groups.group_id.suppressions.get
      x-api-path-slug: asmgroupsgroup-idsuppressions-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Asm
      - Groups
      - Group
      - ""
      - Suppressions
    post:
      summary: Add Asm Groups Group  Suppressions
      description: |-
        **This endpoint allows you to add email addresses to an unsubscribe group.**

        If you attempt to add suppressions to a group that has been deleted or does not exist, the suppressions will be added to the global suppressions list.

        Suppressions are recipient email addresses that are added to [unsubscribe groups](https://sendgrid.com/docs/API_Reference/Web_API_v3/Suppression_Management/groups.html). Once a recipient's address is on the suppressions list for an unsubscribe group, they will not receive any emails that are tagged with that unsubscribe group.
      operationId: asm.groups.group_id.suppressions.post
      x-api-path-slug: asmgroupsgroup-idsuppressions-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Asm
      - Groups
      - Group
      - ""
      - Suppressions
  /asm/groups/{group_id}/suppressions/search:
    post:
      summary: Add Asm Groups Group  Suppressions Search
      description: |-
        **This endpoint allows you to search a suppression group for multiple suppressions.**

        When given a list of email addresses and a group ID, this endpoint will return only the email addresses that have been unsubscribed from the given group.

        Suppressions are a list of email addresses that will not receive content sent under a given [group](https://sendgrid.com/docs/API_Reference/Web_API_v3/Suppression_Management/groups.html).
      operationId: asm.groups.group_id.suppressions.search.post
      x-api-path-slug: asmgroupsgroup-idsuppressionssearch-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Asm
      - Groups
      - Group
      - ""
      - Suppressions
      - Search
  /asm/groups/{group_id}/suppressions/{email}:
    delete:
      summary: Delete Asm Groups Group  Suppressions Email
      description: |-
        **This endpoint allows you to remove a suppressed email address from the given suppression group.**

        Suppressions are recipient email addresses that are added to [unsubscribe groups](https://sendgrid.com/docs/API_Reference/Web_API_v3/Suppression_Management/groups.html). Once a recipient's address is on the suppressions list for an unsubscribe group, they will not receive any emails that are tagged with that unsubscribe group.
      operationId: asm.groups.group_id.suppressions.email.delete
      x-api-path-slug: asmgroupsgroup-idsuppressionsemail-delete
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Asm
      - Groups
      - Group
      - ""
      - Suppressions
      - Email
  /asm/suppressions:
    get:
      summary: Get Asm Suppressions
      description: |-
        **This endpoint allows you to retrieve a list of all suppressions.**

        Suppressions are a list of email addresses that will not receive content sent under a given [group](https://sendgrid.com/docs/API_Reference/Web_API_v3/Suppression_Management/groups.html).
      operationId: asm.suppressions.get
      x-api-path-slug: asmsuppressions-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Asm
      - Suppressions
  /asm/suppressions/global:
    post:
      summary: Add Asm Suppressions Global
      description: |-
        **This endpoint allows you to add one or more email addresses to the global suppressions group.**

        A global suppression (or global unsubscribe) is an email address of a recipient who does not want to receive any of your messages. A globally suppressed recipient will be removed from any email you send. For more information, please see our [User Guide](https://sendgrid.com/docs/User_Guide/Suppressions/global_unsubscribes.html).
      operationId: asm.suppressions.global.post
      x-api-path-slug: asmsuppressionsglobal-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Asm
      - Suppressions
      - Global
  /asm/suppressions/global/{email}:
    delete:
      summary: Delete Asm Suppressions Global Email
      description: |-
        **This endpoint allows you to remove an email address from the global suppressions group.**

        A global suppression (or global unsubscribe) is an email address of a recipient who does not want to receive any of your messages. A globally suppressed recipient will be removed from any email you send. For more information, please see our [User Guide](https://sendgrid.com/docs/User_Guide/Suppressions/global_unsubscribes.html).
      operationId: asm.suppressions.global.email.delete
      x-api-path-slug: asmsuppressionsglobalemail-delete
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Asm
      - Suppressions
      - Global
      - Email
    get:
      summary: Get Asm Suppressions Global Email
      description: |-
        **This endpoint allows you to retrieve a global suppression. You can also use this endpoint to confirm if an email address is already globally suppresed.**

        If the email address you include in the URL path parameter `{email}` is alreayd globally suppressed, the response will include that email address. If the address you enter for `{email}` is not globally suppressed, an empty JSON object `{}` will be returned.

        A global suppression (or global unsubscribe) is an email address of a recipient who does not want to receive any of your messages. A globally suppressed recipient will be removed from any email you send. For more information, please see our [User Guide](https://sendgrid.com/docs/User_Guide/Suppressions/global_unsubscribes.html).
      operationId: asm.suppressions.global.email.get
      x-api-path-slug: asmsuppressionsglobalemail-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Asm
      - Suppressions
      - Global
      - Email
  /asm/suppressions/{email}:
    get:
      summary: Get Asm Suppressions Email
      description: |-
        **This endpoint returns the list of all groups that the given email address has been unsubscribed from.**

        Suppressions are a list of email addresses that will not receive content sent under a given [group](https://sendgrid.com/docs/API_Reference/Web_API_v3/Suppression_Management/groups.html).
      operationId: asm.suppressions.email.get
      x-api-path-slug: asmsuppressionsemail-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Asm
      - Suppressions
      - Email
  /browsers/stats:
    get:
      summary: Get Browsers Stats
      description: |-
        **This endpoint allows you to retrieve your email statistics segmented by browser type.**

        **We only store up to 7 days of email activity in our database.** By default, 500 items will be returned per request via the Advanced Stats API endpoints.

        Advanced Stats provide a more in-depth view of your email statistics and the actions taken by your recipients. You can segment these statistics by geographic location, device type, client type, browser, and mailbox provider. For more information about statistics, please see our [User Guide](https://sendgrid.com/docs/User_Guide/Statistics/index.html).
      operationId: browsers.stats.get
      x-api-path-slug: browsersstats-get
      parameters:
      - in: query
        name: aggregated_by
        description: How to group the stats
      - in: query
        name: browsers
        description: The browsers to get statistics for
      - in: query
        name: end_date
        description: The end date of the statistics to retrieve
      - in: query
        name: limit
        description: The number of results to include on each page
      - in: query
        name: No Name
      - in: query
        name: offset
        description: The number of results to exclude
      - in: query
        name: start_date
        description: The starting date of the statistics to retrieve
      responses:
        200:
          description: OK
      tags:
      - Email
      - Browsers
      - Stats
  /campaigns:
    get:
      summary: Get Campaigns
      description: |-
        **This endpoint allows you to retrieve a list of all of your campaigns.**

        Returns campaigns in reverse order they were created (newest first).

        Returns an empty array if no campaigns exist.

        For more information:

        * [User Guide > Marketing Campaigns](https://sendgrid.com/docs/User_Guide/Marketing_Campaigns/index.html)
      operationId: GET_campaigns
      x-api-path-slug: campaigns-get
      parameters:
      - in: query
        name: limit
        description: The number of results you would like to receive at a time
      - in: query
        name: offset
        description: The index of the first campaign to return, where 0 is the first
          campaign
      responses:
        200:
          description: OK
      tags:
      - Email
      - Campaigns
    post:
      summary: Add Campaigns
      description: |-
        **This endpoint allows you to create a campaign.**

        Our Marketing Campaigns API lets you create, manage, send, and schedule campaigns.

        Note: In order to send or schedule the campaign, you will be required to provide a subject, sender ID, content (we suggest both html and plain text), and at least one list or segment ID. This information is not required when you create a campaign.

        For more information:

        * [User Guide > Marketing Campaigns](https://sendgrid.com/docs/User_Guide/Marketing_Campaigns/index.html)
      operationId: POST_campaigns
      x-api-path-slug: campaigns-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Email
      - Campaigns
  /campaigns/{campaign_id}:
    delete:
      summary: Delete Campaigns Campaign
      description: |-
        **This endpoint allows you to delete a specific campaign.**

        Our Marketing Campaigns API lets you create, manage, send, and schedule campaigns.

        For more information:

        * [User Guide > Marketing Campaigns](https://sendgrid.com/docs/User_Guide/Marketing_Campaigns/index.html)
      operationId: campaigns.campaign_id.delete
      x-api-path-slug: campaignscampaign-id-delete
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Email
      - Campaigns
      - Campaign
    get:
      summary: Get Campaigns Campaign
      description: |-
        **This endpoint allows you to retrieve a specific campaign.**

        Our Marketing Campaigns API lets you create, manage, send, and schedule campaigns.

        For more information:

        * [User Guide > Marketing Campaigns](https://sendgrid.com/docs/User_Guide/Marketing_Campaigns/index.html)
      operationId: campaigns.campaign_id.get
      x-api-path-slug: campaignscampaign-id-get
      responses:
        200:
          description: OK
      tags:
      - Email
      - Campaigns
      - Campaign
    patch:
      summary: Patch Campaigns Campaign
      description: |-
        Update a campaign. This is especially useful if you only set up the campaign using POST /campaigns, but didn't set many of the parameters.

        For more information:

        * [User Guide > Marketing Campaigns](https://sendgrid.com/docs/User_Guide/Marketing_Campaigns/index.html)
      operationId: campaigns.campaign_id.patch
      x-api-path-slug: campaignscampaign-id-patch
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Email
      - Campaigns
      - Campaign
  /campaigns/{campaign_id}/schedules:
    delete:
      summary: Delete Campaigns Campaign  Schedules
      description: |-
        **This endpoint allows you to unschedule a campaign that has already been scheduled to be sent.**

        A successful unschedule will return a 204.
        If the specified campaign is in the process of being sent, the only option is to cancel (a different method).

        For more information:

        * [User Guide > Marketing Campaigns](https://sendgrid.com/docs/User_Guide/Marketing_Campaigns/index.html)
      operationId: campaigns.campaign_id.schedules.delete
      x-api-path-slug: campaignscampaign-idschedules-delete
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Email
      - Campaigns
      - Campaign
      - ""
      - Schedules
    get:
      summary: Get Campaigns Campaign  Schedules
      description: |-
        **This endpoint allows you to retrieve the date and time that the given campaign has been scheduled to be sent.**

        For more information:

        * [User Guide > Marketing Campaigns](https://sendgrid.com/docs/User_Guide/Marketing_Campaigns/index.html)
      operationId: campaigns.campaign_id.schedules.get
      x-api-path-slug: campaignscampaign-idschedules-get
      responses:
        200:
          description: OK
      tags:
      - Email
      - Campaigns
      - Campaign
      - ""
      - Schedules
    patch:
      summary: Patch Campaigns Campaign  Schedules
      description: |-
        **This endpoint allows to you change the scheduled time and date for a campaign to be sent.**

        For more information:

        * [User Guide > Marketing Campaigns](https://sendgrid.com/docs/User_Guide/Marketing_Campaigns/index.html)
      operationId: campaigns.campaign_id.schedules.patch
      x-api-path-slug: campaignscampaign-idschedules-patch
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Email
      - Campaigns
      - Campaign
      - ""
      - Schedules
    post:
      summary: Add Campaigns Campaign  Schedules
      description: |-
        **This endpoint allows you to schedule a specific date and time for your campaign to be sent.**

        For more information:

        * [User Guide > Marketing Campaigns](https://sendgrid.com/docs/User_Guide/Marketing_Campaigns/index.html)
      operationId: campaigns.campaign_id.schedules.post
      x-api-path-slug: campaignscampaign-idschedules-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Email
      - Campaigns
      - Campaign
      - ""
      - Schedules
  /campaigns/{campaign_id}/schedules/now:
    post:
      summary: Add Campaigns Campaign  Schedules Now
      description: |-
        **This endpoint allows you to immediately send a campaign at the time you make the API call.**

        Normally a POST would have a request body, but since this endpoint is telling us to send a resource that is already created, a request body is not needed.

        For more information:

        * [User Guide > Marketing Campaigns](https://sendgrid.com/docs/User_Guide/Marketing_Campaigns/index.html)
      operationId: campaigns.campaign_id.schedules.now.post
      x-api-path-slug: campaignscampaign-idschedulesnow-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Email
      - Campaigns
      - Campaign
      - ""
      - Schedules
      - Now
  /campaigns/{campaign_id}/schedules/test:
    post:
      summary: Add Campaigns Campaign  Schedules Test
      description: |-
        **This endpoint allows you to send a test campaign.**

        To send to multiple addresses, use an array for the JSON "to" value ["one@address","two@address"]

        For more information:

        * [User Guide > Marketing Campaigns](https://sendgrid.com/docs/User_Guide/Marketing_Campaigns/index.html)
      operationId: campaigns.campaign_id.schedules.test.post
      x-api-path-slug: campaignscampaign-idschedulestest-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Email
      - Campaigns
      - Campaign
      - ""
      - Schedules
      - Test
  /categories:
    get:
      summary: Get Categories
      description: "**This endpoint allows you to retrieve a list of all of your categories.**\n\nCategories
        can help organize your email analytics by enabling you to \u201Ctag\u201D
        emails by type or broad topic. You can define your own custom categories.
        For more information, please see our [User Guide](https://sendgrid.com/docs/User_Guide/Statistics/categories.html)."
      operationId: GET_categories
      x-api-path-slug: categories-get
      parameters:
      - in: query
        name: category
        description: Allows you to perform a prefix search on this particular category
      - in: query
        name: limit
        description: The number of categories to display per page
      - in: query
        name: No Name
      - in: query
        name: offset
        description: The point in the list that you would like to begin displaying
          results
      responses:
        200:
          description: OK
      tags:
      - Email
      - Categories
  /categories/stats:
    get:
      summary: Get Categories Stats
      description: |-
        **This endpoint allows you to retrieve all of your email statistics for each of your categories.**

        If you do not define any query parameters, this endpoint will return a sum for each category in groups of 10.

        Categories allow you to group your emails together according to broad topics that you define. For more information, please see our [User Guide](https://sendgrid.com/docs/User_Guide/Statistics/categories.html).
      operationId: categories.stats.get
      x-api-path-slug: categoriesstats-get
      parameters:
      - in: query
        name: aggregated_by
        description: How to group the statistics
      - in: query
        name: categories
        description: The individual categories that you want to retrieve statistics
          for
      - in: query
        name: end_date
        description: The end date of the statistics to retrieve
      - in: query
        name: limit
        description: The number of results to include
      - in: query
        name: No Name
      - in: query
        name: offset
        description: The number of results to skip
      - in: query
        name: start_date
        description: The starting date of the statistics to retrieve
      responses:
        200:
          description: OK
      tags:
      - Email
      - Categories
      - Stats
  /categories/stats/sums:
    get:
      summary: Get Categories Stats Sums
      description: |-
        **This endpoint allows you to retrieve the total sum of each email statistic for every category over the given date range.**

        If you do not define any query parameters, this endpoint will return a sum for each category in groups of 10.

        Categories allow you to group your emails together according to broad topics that you define. For more information, please see our [User Guide](https://sendgrid.com/docs/User_Guide/Statistics/categories.html).
      operationId: categories.stats.sums.get
      x-api-path-slug: categoriesstatssums-get
      parameters:
      - in: query
        name: aggregated_by
        description: How to group the statistics
      - in: query
        name: end_date
        description: The end date of the statistics to retrieve
      - in: query
        name: limit
        description: Limits the number of results returned
      - in: query
        name: No Name
      - in: query
        name: offset
        description: The point in the list to begin retrieving results
      - in: query
        name: sort_by_direction
        description: The direction you want to sort
      - in: query
        name: sort_by_metric
        description: The metric that you want to sort by
      - in: query
        name: start_date
        description: The starting date of the statistics to retrieve
      responses:
        200:
          description: OK
      tags:
      - Email
      - Categories
      - Stats
      - Sums
  /clients/stats:
    get:
      summary: Get Clients Stats
      description: |-
        **This endpoint allows you to retrieve your email statistics segmented by client type.**

        **We only store up to 7 days of email activity in our database.** By default, 500 items will be returned per request via the Advanced Stats API endpoints.

        Advanced Stats provide a more in-depth view of your email statistics and the actions taken by your recipients. You can segment these statistics by geographic location, device type, client type, browser, and mailbox provider. For more information about statistics, please see our [User Guide](https://sendgrid.com/docs/User_Guide/Statistics/index.html).
      operationId: clients.stats.get
      x-api-path-slug: clientsstats-get
      parameters:
      - in: query
        name: aggregated_by
        description: How to group the statistics
      - in: query
        name: end_date
        description: The end date of the statistics to retrieve
      - in: query
        name: No Name
      - in: query
        name: start_date
        description: The starting date of the statistics to retrieve
      responses:
        200:
          description: OK
      tags:
      - Email
      - Clients
      - Stats
  /clients/{client_type}/stats:
    get:
      summary: Get Clients Client Type Stats
      description: |-
        **This endpoint allows you to retrieve your email statistics segmented by a specific client type.**

        **We only store up to 7 days of email activity in our database.** By default, 500 items will be returned per request via the Advanced Stats API endpoints.

        ## Available Client Types
        - phone
        - tablet
        - webmail
        - desktop

        Advanced Stats provide a more in-depth view of your email statistics and the actions taken by your recipients. You can segment these statistics by geographic location, device type, client type, browser, and mailbox provider. For more information about statistics, please see our [User Guide](https://sendgrid.com/docs/User_Guide/Statistics/index.html).
      operationId: clients.client_type.stats.get
      x-api-path-slug: clientsclient-typestats-get
      parameters:
      - in: query
        name: aggregated_by
        description: How to group the statistics
      - in: query
        name: end_date
        description: The end date of the statistics to retrieve
      - in: query
        name: No Name
      - in: query
        name: start_date
        description: The starting date of the statistics to retrieve
      responses:
        200:
          description: OK
      tags:
      - Email
      - Clients
      - Client
      - Type
      - Stats
  /contactdb/custom_fields:
    get:
      summary: Get Contactdb Custom Fields
      description: "**This endpoint allows you to retrieve all custom fields.** \n\nThe
        contactdb is a database of your contacts for [SendGrid Marketing Campaigns](https://sendgrid.com/docs/User_Guide/Marketing_Campaigns/index.html)."
      operationId: contactdb.custom_fields.get
      x-api-path-slug: contactdbcustom-fields-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Contactdb
      - Custom
      - Fields
    post:
      summary: Add Contactdb Custom Fields
      description: |-
        **This endpoint allows you to create a custom field.**

        The contactdb is a database of your contacts for [SendGrid Marketing Campaigns](https://sendgrid.com/docs/User_Guide/Marketing_Campaigns/index.html).
      operationId: contactdb.custom_fields.post
      x-api-path-slug: contactdbcustom-fields-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Contactdb
      - Custom
      - Fields
  /contactdb/custom_fields/{custom_field_id}:
    delete:
      summary: Delete Contactdb Custom Fields Custom Field
      description: |-
        **This endpoint allows you to delete a custom field by ID.**

        The contactdb is a database of your contacts for [SendGrid Marketing Campaigns](https://sendgrid.com/docs/User_Guide/Marketing_Campaigns/index.html).
      operationId: contactdb.custom_fields.custom_field_id.delete
      x-api-path-slug: contactdbcustom-fieldscustom-field-id-delete
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Contactdb
      - Custom
      - Fields
      - Custom
      - Field
    get:
      summary: Get Contactdb Custom Fields Custom Field
      description: |-
        **This endpoint allows you to retrieve a custom field by ID.**

        The contactdb is a database of your contacts for [SendGrid Marketing Campaigns](https://sendgrid.com/docs/User_Guide/Marketing_Campaigns/index.html).
      operationId: contactdb.custom_fields.custom_field_id.get
      x-api-path-slug: contactdbcustom-fieldscustom-field-id-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Contactdb
      - Custom
      - Fields
      - Custom
      - Field
  /contactdb/lists:
    delete:
      summary: Delete Contactdb Lists
      description: |-
        **This endpoint allows you to delete multiple recipient lists.**

        The Contacts API helps you manage your [Marketing Campaigns](https://sendgrid.com/docs/User_Guide/Marketing_Campaigns/index.html) recipients.
      operationId: contactdb.lists.delete
      x-api-path-slug: contactdblists-delete
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Contactdb
      - Lists
    get:
      summary: Get Contactdb Lists
      description: |-
        **This endpoint allows you to retrieve all of your recipient lists. If you don't have any lists, an empty array will be returned.**

        The Contacts API helps you manage your [Marketing Campaigns](https://sendgrid.com/docs/User_Guide/Marketing_Campaigns/index.html) recipients.
      operationId: contactdb.lists.get
      x-api-path-slug: contactdblists-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Contactdb
      - Lists
    post:
      summary: Add Contactdb Lists
      description: |-
        **This endpoint allows you to create a list for your recipients.**

        The Contacts API helps you manage your [Marketing Campaigns](https://sendgrid.com/docs/User_Guide/Marketing_Campaigns/index.html) recipients.
      operationId: contactdb.lists.post
      x-api-path-slug: contactdblists-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Contactdb
      - Lists
  /contactdb/lists/{list_id}:
    delete:
      summary: Delete Contactdb Lists List
      description: |-
        **This endpoint allows you to delete a specific recipient list with the given ID.**

        The Contacts API helps you manage your [Marketing Campaigns](https://sendgrid.com/docs/User_Guide/Marketing_Campaigns/index.html) recipients.
      operationId: contactdb.lists.list_id.delete
      x-api-path-slug: contactdblistslist-id-delete
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: delete_contacts
        description: Adds the ability to delete all contacts on the list in addition
          to deleting the list
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Contactdb
      - Lists
      - List
    get:
      summary: Get Contactdb Lists List
      description: |-
        This endpoint allows you to retrieve a single recipient list.

        The Contacts API helps you manage your [Marketing Campaigns](https://sendgrid.com/docs/User_Guide/Marketing_Campaigns/index.html) recipients.
      operationId: contactdb.lists.list_id.get
      x-api-path-slug: contactdblistslist-id-get
      parameters:
      - in: query
        name: list_id
        description: The ID of the list to retrieve
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Contactdb
      - Lists
      - List
    patch:
      summary: Patch Contactdb Lists List
      description: |-
        **This endpoint allows you to update the name of one of your recipient lists.**


        The Contacts API helps you manage your [Marketing Campaigns](https://sendgrid.com/docs/User_Guide/Marketing_Campaigns/index.html) recipients.
      operationId: contactdb.lists.list_id.patch
      x-api-path-slug: contactdblistslist-id-patch
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: list_id
        description: The ID of the list you are updating
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Contactdb
      - Lists
      - List
  /contactdb/lists/{list_id}/recipients:
    get:
      summary: Get Contactdb Lists List  Recipients
      description: "**This endpoint allows you to retrieve all recipients on the list
        with the given ID.** \n\nThe Contacts API helps you manage your [Marketing
        Campaigns](https://sendgrid.com/docs/User_Guide/Marketing_Campaigns/index.html)
        recipients."
      operationId: contactdb.lists.list_id.recipients.get
      x-api-path-slug: contactdblistslist-idrecipients-get
      parameters:
      - in: query
        name: list_id
        description: The ID of the list whose recipients you are requesting
      - in: query
        name: No Name
      - in: query
        name: page
        description: Page index of first recipient to return (must be a positive integer)
      - in: query
        name: page_size
        description: Number of recipients to return at a time (must be a positive
          integer between 1 and 1000)
      responses:
        200:
          description: OK
      tags:
      - Email
      - Contactdb
      - Lists
      - List
      - ""
      - Recipients
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---