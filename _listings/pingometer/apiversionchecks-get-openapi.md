---
swagger: "2.0"
x-collection-name: Pingometer
x-complete: 0
info:
  title: Checks API Get Check List
  description: Returns a list overview of all checks.
  version: 1.0.0
host: api.pingdom.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  '/checks ':
    ' get ':
      summary: Checks
      description: Gets a list of all checks that are visible to you as a user or
        a customer depending on the request context.
      operationId: -checks-
      x-api-path-slug: checks-get
      responses:
        200:
          description: OK
      tags:
      - Checks
  '/checks/{checkId} ':
    ' get ':
      summary: Checks {checkId}
      description: Gets info about a check, current SLA, last result and its status.
      operationId: -checks-checkid-
      x-api-path-slug: checkscheckid-get
      responses:
        200:
          description: OK
      tags:
      - Checks
    ' put ':
      summary: Checks {checkId}
      description: Updates a check.
      operationId: -checks-checkid-
      x-api-path-slug: checkscheckid-put
      responses:
        200:
          description: OK
      tags:
      - Checks
    ' delete ':
      summary: Checks {checkId}
      description: Deletes a check.
      operationId: -checks-checkid-
      x-api-path-slug: checkscheckid-delete
      responses:
        200:
          description: OK
      tags:
      - Checks
  '/checks/{checkId}/lastvalue ':
    ' get ':
      summary: Checks {checkId} Lastvalue
      description: Gets the absolute last value of a specific check.
      operationId: -checks-checkid-lastvalue-
      x-api-path-slug: checkscheckidlastvalue-get
      responses:
        200:
          description: OK
      tags:
      - Checks
  '/checks/{checkId}/results/{millisecondsUtc}?detail_level={detail_level} ':
    ' get ':
      summary: Checks {checkId} Results {millisecondsUtc}?detail_level={detail_level}
      description: Gets a specific check result by a numeric java timestamp.
      operationId: -checks-checkid-results-millisecondsutcdetail-leveldetail-level-
      x-api-path-slug: checkscheckidresultsmillisecondsutcdetail-leveldetail-level-get
      responses:
        200:
          description: OK
      tags:
      - Checks
  '/checks/{checkId}/results?mostrecent={mostrecent}&amp;detail_level={detail_level} ':
    ' get ':
      summary: Checks {checkId} Results?mostrecent={mostrecent}&amp;detail_level={detail_level}
      description: Gets the most recent check results.
      operationId: -checks-checkid-resultsmostrecentmostrecentampdetail-leveldetail-level-
      x-api-path-slug: checkscheckidresultsmostrecentmostrecentampdetail-leveldetail-level-get
      responses:
        200:
          description: OK
      tags:
      - Checks
  '/checks/{checkId}/results?fromUtc={fromUtc}&amp;toUtc={toUtc}&amp;detail_level={detail_level} ':
    ' get ':
      summary: Checks {checkId} Results?fromUtc={fromUtc}&amp;toUtc={toUtc}&amp;detail_level={detail_level}
      description: Gets check results between two dates.
      operationId: -checks-checkid-resultsfromutcfromutcamptoutctoutcampdetail-leveldetail-level-
      x-api-path-slug: checkscheckidresultsfromutcfromutcamptoutctoutcampdetail-leveldetail-level-get
      responses:
        200:
          description: OK
      tags:
      - Checks
  ? |2-

        /api/{version}/checks
  : ? |2-

          get
    : summary: Get Check List
      description: Returns a list overview of all checks.
      operationId: get-check-list
      x-api-path-slug: apiversionchecks-get
      parameters:
      - in: query
        name: include_tags
        description: Include tag list for each check
        type: <td>boolean</td>
      - in: query
        name: limit
        description: Limits the number of returned probes to the specified quantity
        type: <td>integer</td>
      - in: query
        name: offset
        description: Offset for listing
        type: <td>integer</td>
      - in: query
        name: tags
        description: Tag list separated by commas
        type: <td>string</td>
      responses:
        200:
          description: OK
      tags:
      - Checks
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