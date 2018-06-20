---
swagger: "2.0"
x-collection-name: Microsoft Graph
x-complete: 0
info:
  title: Microsoft Graph Delete Mail Folder
  description: Delete mailFolder Delete mailFolder.
  version: 1.0.0
host: graph.microsoft.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /groups/{id}/subscribeByMail:
    post:
      summary: Group Subscribe By Mail
      description: 'group: subscribeByMail Calling this method will enable the current
        user to receive email notifications for this group, about new posts, events,
        and files in that group. Supported for only Office 365 groups.'
      operationId: Group:SubscribeByMail
      x-api-path-slug: groupsidsubscribebymail-post
      parameters:
      - in: header
        name: Authorization
        description: 'Bearer '
      - in: path
        name: id
        type: string
      responses:
        200:
          description: OK
      tags:
      - Group
      - SubscribeMail
  /groups/{id}/unsubscribeByMail:
    post:
      summary: Group Unsubscribe By Mail
      description: 'group: unsubscribeByMail Calling this method will prevent the
        current user from receiving email notifications for this group about new posts,
        events, and files in that group. Supported for only Office 365 groups.'
      operationId: Group:UnsubscribeByMail
      x-api-path-slug: groupsidunsubscribebymail-post
      parameters:
      - in: header
        name: Authorization
        description: 'Bearer '
      - in: path
        name: id
        type: string
      responses:
        200:
          description: OK
      tags:
      - Group
      - UnsubscribeMail
  /me/mailFolders/{id}/copy:
    post:
      summary: Mail Folder Copy
      description: 'mailFolder: copy Copy a mailfolder and its contents to another
        mailfolder.'
      operationId: MailFolder:Copy
      x-api-path-slug: memailfoldersidcopy-post
      parameters:
      - in: header
        name: Authorization
        description: 'Bearer '
      - in: header
        name: Content-Type
        description: application/json
      - in: path
        name: id
        type: string
      responses:
        200:
          description: OK
      tags:
      - Mail
      - Folder
      - Copy
  /users/{id | userPrincipalName}/mailFolders/{id}/copy:
    post:
      summary: Mail Folder Copy
      description: 'mailFolder: copy Copy a mailfolder and its contents to another
        mailfolder.'
      operationId: MailFolder:Copy
      x-api-path-slug: usersid--userprincipalnamemailfoldersidcopy-post
      parameters:
      - in: header
        name: Authorization
        description: 'Bearer '
      - in: header
        name: Content-Type
        description: application/json
      - in: path
        name: id
        type: string
      - in: path
        name: id | userPrincipalName
        type: string
      responses:
        200:
          description: OK
      tags:
      - Mail
      - Folder
      - Copy
  /me/mailFolders/{id}:
    delete:
      summary: Delete Mail Folder
      description: Delete mailFolder Delete mailFolder.
      operationId: DeleteMailFolder
      x-api-path-slug: memailfoldersid-delete
      parameters:
      - in: header
        name: Authorization
        description: 'Bearer '
        type: string
      - in: path
        name: id
        type: string
      responses:
        200:
          description: OK
      tags:
      - Mail
      - Folder
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