swagger: "2.0"
x-collection-name: SendGrid
x-complete: 1
info:
  title: SendGrid
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
  /subusers/stats/monthly:
    get:
      summary: Get Subusers Stats Monthly
      description: |-
        **This endpoint allows you to retrieve the monthly email statistics for all subusers over the given date range.**

        While you can always view the statistics for all email activity on your account, subuser statistics enable you to view specific segments of your stats for your subusers. Emails sent, bounces, and spam reports are always tracked for subusers. Unsubscribes, clicks, and opens are tracked if you have enabled the required settings.

        When using the `sort_by_metric` to sort your stats by a specific metric, you can not sort by the following metrics:
        `bounce_drops`, `deferred`, `invalid_emails`, `processed`, `spam_report_drops`, `spam_reports`, or `unsubscribe_drops`.

        For more information, see our [User Guide](https://sendgrid.com/docs/User_Guide/Statistics/subuser.html).
      operationId: subusers.stats.monthly.get
      x-api-path-slug: subusersstatsmonthly-get
      parameters:
      - in: query
        name: date
        description: The date of the month to retrieve statistics for
      - in: query
        name: limit
        description: Optional field to limit the number of results returned
      - in: query
        name: offset
        description: Optional beginning point in the list to retrieve from
      - in: query
        name: sort_by_direction
        description: The direction you want to sort
      - in: query
        name: sort_by_metric
        description: The metric that you want to sort by
      - in: query
        name: subuser
        description: A substring search of your subusers
      responses:
        200:
          description: OK
      tags:
      - Email
      - Subusers
      - Stats
      - Monthly
  /subusers/{subuser_name}/stats/monthly:
    get:
      summary: Get Subusers Subuser Name Stats Monthly
      description: |-
        **This endpoint allows you to retrive the monthly email statistics for a specific subuser.**

        While you can always view the statistics for all email activity on your account, subuser statistics enable you to view specific segments of your stats for your subusers. Emails sent, bounces, and spam reports are always tracked for subusers. Unsubscribes, clicks, and opens are tracked if you have enabled the required settings.

        When using the `sort_by_metric` to sort your stats by a specific metric, you can not sort by the following metrics:
        `bounce_drops`, `deferred`, `invalid_emails`, `processed`, `spam_report_drops`, `spam_reports`, or `unsubscribe_drops`.

        For more information, see our [User Guide](https://sendgrid.com/docs/User_Guide/Statistics/subuser.html).
      operationId: subusers.subuser_name.stats.monthly.get
      x-api-path-slug: subuserssubuser-namestatsmonthly-get
      parameters:
      - in: query
        name: date
        description: The date of the month to retrieve statistics for
      - in: query
        name: limit
        description: Optional field to limit the number of results returned
      - in: query
        name: offset
        description: Optional beginning point in the list to retrieve from
      - in: query
        name: sort_by_direction
        description: The direction you want to sort
      - in: query
        name: sort_by_metric
        description: The metric that you want to sort by
      responses:
        200:
          description: OK
      tags:
      - Email
      - Subusers
      - Subuser
      - Name
      - Stats
      - Monthly