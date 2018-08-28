swagger: "2.0"
x-collection-name: 3dcart
x-complete: 1
info:
  title: _3dCartWebAPI
  version: 1.0.0
host: apirest.3dcart.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /3dCartWebAPI/v1/GiftRegistries:
    get:
      summary: Get all GiftRegistries
      description: Get all giftregistries.
      operationId: GiftRegistries_GetAllGiftRegistries
      x-api-path-slug: 3dcartwebapiv1giftregistries-get
      parameters:
      - in: query
        name: catalogid
        description: Catalog ID
      - in: query
        name: countonly
        description: Count the number of rows only
      - in: query
        name: dateendcreated
        description: Created Date End (mm/dd/yyyy hh:mm:ss)
      - in: query
        name: dateendevent
        description: Event Date End (mm/dd/yyyy hh:mm:ss)
      - in: query
        name: dateendexpiration
        description: Expiration Date End (mm/dd/yyyy hh:mm:ss)
      - in: query
        name: datestartcreated
        description: Created Date Start (mm/dd/yyyy hh:mm:ss)
      - in: query
        name: datestartevent
        description: Event Date Start (mm/dd/yyyy hh:mm:ss)
      - in: query
        name: datestartexpiration
        description: Expiration Date Start (mm/dd/yyyy hh:mm:ss)
      - in: query
        name: limit
        description: Maximum number of items that can be returned
      - in: query
        name: offset
        description: Starting point for the return data
      - in: header
        name: PrivateKey
        description: PrivateKey
      - in: header
        name: SecureURL
        description: SecureURL
      - in: query
        name: sku
        description: SKU Code of the product
      - in: header
        name: Token
        description: Token
      responses:
        200:
          description: OK
      tags:
      - GiftRegistries
  /3dCartWebAPI/v1/GiftRegistries/{giftregistryid}:
    get:
      summary: Get a specific GiftRegistry
      description: Get a specific giftregistry.
      operationId: GiftRegistries_GetGiftRegistry
      x-api-path-slug: 3dcartwebapiv1giftregistriesgiftregistryid-get
      parameters:
      - in: path
        name: giftregistryid
        description: Gift Resitry ID
      - in: header
        name: PrivateKey
        description: PrivateKey
      - in: header
        name: SecureURL
        description: SecureURL
      - in: header
        name: Token
        description: Token
      responses:
        200:
          description: OK
      tags:
      - Specific
      - GiftRegistry
  /3dCartWebAPI/v1/GiftRegistries/{giftregistryid}/Items:
    get:
      summary: Gets the items from a specific Gift Registry
      description: Gets the items from a specific gift registry.
      operationId: GiftRegistries_GetAllGiftRegistryItem
      x-api-path-slug: 3dcartwebapiv1giftregistriesgiftregistryiditems-get
      parameters:
      - in: path
        name: giftregistryid
        description: Gift Registry ID
      - in: query
        name: limit
        description: Maximum number of items that can be returned
      - in: query
        name: offset
        description: Starting point for the return data
      - in: header
        name: PrivateKey
        description: PrivateKey
      - in: header
        name: SecureURL
        description: SecureURL
      - in: header
        name: Token
        description: Token
      responses:
        200:
          description: OK
      tags:
      - S
      - Items
      - From
      - Specific
      - Gift
      - Registry