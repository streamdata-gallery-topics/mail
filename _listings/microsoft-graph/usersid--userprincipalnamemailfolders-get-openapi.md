---
swagger: "2.0"
x-collection-name: Microsoft Graph
x-complete: 0
info:
  title: Microsoft Graph List Mail Folders
  description: List mailFolders Get the mail folder collection under the root folder
    of the signed-in user.
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
    get:
      summary: Get Mail Folder
      description: Get mailFolder Retrieve the properties and relationships of mailfolder
        object.
      operationId: GetMailFolder
      x-api-path-slug: memailfoldersid-get
      parameters:
      - in: query
        name: $expand
        type: string
      - in: header
        name: Authorization
        description: Bearer
      - in: path
        name: id
        type: string
      responses:
        200:
          description: OK
      tags:
      - Mail
      - Folder
  /users/{id | userPrincipalName}/mailFolders/{id}:
    delete:
      summary: Delete Mail Folder
      description: Delete mailFolder Delete mailFolder.
      operationId: DeleteMailFolder
      x-api-path-slug: usersid--userprincipalnamemailfoldersid-delete
      parameters:
      - in: header
        name: Authorization
        description: 'Bearer '
        type: string
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
    get:
      summary: Get Mail Folder
      description: Get mailFolder Retrieve the properties and relationships of mailfolder
        object.
      operationId: GetMailFolder
      x-api-path-slug: usersid--userprincipalnamemailfoldersid-get
      parameters:
      - in: header
        name: Authorization
        description: 'Bearer '
        type: string
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
  /me/mailFolders/{id}/move:
    post:
      summary: Mail Folder Move
      description: 'mailFolder: move Move a mailfolder and its contents to another
        mailfolder.'
      operationId: MailFolder:Move
      x-api-path-slug: memailfoldersidmove-post
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
      - Move
  /users/{id | userPrincipalName}/mailFolders/{id}/move:
    post:
      summary: Mail Folder Move
      description: 'mailFolder: move Move a mailfolder and its contents to another
        mailfolder.'
      operationId: MailFolder:Move
      x-api-path-slug: usersid--userprincipalnamemailfoldersidmove-post
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
      - Move
  /me/mailFolders/{id}/childFolders:
    post:
      summary: Create Mail Folder
      description: Create MailFolder Use this API to create a new child mailfolder.
      operationId: CreateMailFolder
      x-api-path-slug: memailfoldersidchildfolders-post
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
  /users/{id | userPrincipalName}/mailFolders/{id}/childFolders:
    post:
      summary: Create Mail Folder
      description: Create MailFolder Use this API to create a new child mailfolder.
      operationId: CreateMailFolder
      x-api-path-slug: usersid--userprincipalnamemailfoldersidchildfolders-post
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
  /users/{id | userPrincipalName}/mailFolders:
    get:
      summary: List Mail Folders
      description: List mailFolders Get the mail folder collection under the root
        folder of the signed-in user.
      operationId: ListMailFolders
      x-api-path-slug: usersid--userprincipalnamemailfolders-get
      parameters:
      - in: header
        name: Authorization
        description: 'Bearer '
      - in: header
        name: Content-Type
        description: application/json
      - in: path
        name: id | userPrincipalName
        type: string
      responses:
        200:
          description: OK
      tags:
      - List
      - Mail
      - Folders
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