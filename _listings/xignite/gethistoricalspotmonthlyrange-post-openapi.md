---
swagger: "2.0"
x-collection-name: Xignite
x-complete: 0
info:
  title: Xignite Futures Get Historical Spot Monthly Range
  description: Returns a range of commodity spot prices for a commodity.
  version: 1.0.0
host: www.xignite.com
basePath: xFutures.json/XigniteFutures
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /GetHistoricalCommodityMonthlyRange:
    post:
      summary: Get Historical Commodity Monthly Range
      description: Returns a range of historical quotes for a future contract.
      operationId: postGethistoricalcommoditymonthlyrange
      x-api-path-slug: gethistoricalcommoditymonthlyrange-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Historical
      - Commodity
      - Monthly
      - Range
  /GetHistoricalSpotMonthlyRange:
    post:
      summary: Get Historical Spot Monthly Range
      description: Returns a range of commodity spot prices for a commodity.
      operationId: postGethistoricalspotmonthlyrange
      x-api-path-slug: gethistoricalspotmonthlyrange-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Historical
      - Spot
      - Monthly
      - Range
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