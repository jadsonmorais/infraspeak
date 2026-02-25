![Spinner: White decorative](https://cdn.userway.org/widgetapp/images/spin_wh.svg)

![](https://cdn.userway.org/widgetapp/images/body_wh.svg)

![Spinner: White decorative](https://cdn.userway.org/widgetapp/images/spin_wh.svg)

Frame

# Status embed installed correctly

This will be shown if an incident or maintenance is posted on your status page.


[View latest updates](https://stoplight.status.smartbear.com/?utm_source=embed)

[![Stoplight logo](https://infraspeak.stoplight.io/static/images/logo-blue-white.png)](https://stoplight.io/?utm_source=workspaces&utm_medium=referral&utm_campaign=free_workspace_banner)

[Like what you see? Create your own free Stoplight workspace to start documenting and designing APIs today.](https://stoplight.io/welcome?utm_source=workspaces&utm_medium=referral&utm_campaign=free_workspace_banner)

Create a Workspace

# List all Failures

get

https://api.infraspeak.com/v3/failures

This endpoint allows you to list all Failures.

The query parameters described below are to be used with the [JQL](https://infraspeak.stoplight.io/docs/api/1f866ecae49d8-parameters).

## [Request](https://infraspeak.stoplight.io/docs/api/1405a02f5beb9-list-all-failures\#Request)

Security: Bearer Auth

### [Query Parameters](https://infraspeak.stoplight.io/docs/api/1405a02f5beb9-list-all-failures\#Query-Parameters)

approved\_date

string<date-time>

Filter results by the approval date of the Failure.

completed\_date

string<date-time>

Filter results by the completion date of the Failure.

failure\_id

integer

Filter results by the ID of the Failure

last\_status\_change\_date

string<date-time>

Filter results by the last status change date of the Failure.

local\_id

integer

Filter results by the local of the Failure.

problem\_id

integer

Filter results by the problem of the Failure.

start\_date

string<date-time>

Filter results by the date of report of the Failure.

status

string

Filter results by the status of the Failure.

Allowed values:

WAITING\_APPROVALWAITING\_RESOLUTIONIN\_RESOLUTIONPAUSEDCOMPLETEDARCHIVED

## [Responses](https://infraspeak.stoplight.io/docs/api/1405a02f5beb9-list-all-failures\#Responses)

200

400

401

429

500

OK

### [Body](https://infraspeak.stoplight.io/docs/api/1405a02f5beb9-list-all-failures\#response-body)

application/json

application/json

data

array\[Failure\]

id

string

required

ID of the Failure

type

any

required

Model type

Allowed value:

failure

attributes

object

required

relationships

object

included

array (anyOf) \[File\]array (anyOf) \[Location\]array (anyOf) \[Operator\]

array (anyOf) \[File\]

File model structure details

id

string

required

ID of the File

type

any

required

Model type

Allowed value:

file

attributes

object

required

meta

Meta

Meta model structure details

pagination

object

links

Response Links on listing operations

Requests that return multiple items include a `links` attribute, with links related to request's context.

self

string

required

Current response link.

Example:

/path?page=1

first

string

required

Link to the first page result.

Example:

/path?page=1

last

string

required

Link to the previous page result.

Example:

/path?page=1

next

string

Link to the next page result.

Example:

/path?page=1

Auth

Token:

Parameters

approved\_date:

completed\_date:

failure\_id:

last\_status\_change\_date:

local\_id:

problem\_id:

start\_date:

status:

Not SetWAITING\_APPROVALWAITING\_RESOLUTIONIN\_RESOLUTIONPAUSEDCOMPLETEDARCHIVED

select an option

Send API Request

Production

Request Sample: Shell / cURL

```
curl --request GET \

  --url https://api.infraspeak.com/v3/failures \

  --header 'Accept: application/json' \

  --header 'Authorization: Bearer 123'
```

Response Example

```
1
{

2
  "data": [\
\
3\
    {\
\
4\
      "id": "string",\
\
5\
      "type": "failure",\
\
6\
      "attributes": {\
\
7\
        "failure_id": 1,\
\
8\
        "uuid": "095be615-a8ad-4c33-8e9c-c7612fbf6c9f",\
\
9\
        "problem_id": 0,\
\
10\
        "status": "WAITING_APPROVAL",\
\
11\
        "start_date": "2020-08-28T08:48:00.000Z",\
\
12\
        "completed_date": "2020-08-28T17:12:00.000Z",\
\
13\
        "approved_date": "2020-08-28T09:30:00.000Z",\
\
14\
        "paused_date": "2020-08-28T13:05:00.000Z",\
\
15\
        "description": "Needs replacement",\
\
16\
        "last_status_description": "Completed",\
\
17\
        "observations": "Needs a new part",\
\
18\
        "code": "WO2022",\
\
19\
        "fts_vector": "string",\
\
20\
        "priority": 1,\
\
21\
        "client_id": 0,\
\
22\
        "entity_id": 0,\
\
23\
        "metering_registry_id": 0,\
\
24\
        "local_id": 0,\
\
25\
        "paused_reason_id": 0,\
\
26\
        "external_id": "string",\
\
27\
        "report_name": "string",\
\
28\
        "solved": false,\
\
29\
        "confirmed": false,\
\
30\
        "started": false,\
\
31\
        "paused": false,\
\
32\
        "completed": false,\
\
33\
        "archived": false,\
\
34\
        "approved": false,\
\
35\
        "next_schedule": "2020-08-29T10:30:00.000Z",\
\
36\
        "message_count": 0,\
\
37\
        "time_statistics": {\
\
38\
          "approved_date": "2020-08-28T09:30:00.000Z",\
\
39\
          "last_completed_date": "2020-08-28T17:12:00.000Z",\
\
40\
          "last_paused_date": "2020-08-28T13:05:00.000Z",\
\
41\
          "started_date": "2020-08-28T09:45:00.000Z",\
\
42\
          "time_to_approve": "P0Y0M0DT0H42M0S",\
\
43\
          "time_to_complete": "P0Y0M0DT8H24M0S",\
\
44\
          "time_to_complete_after_started": "P0Y0M0DT7H27M0S",\
\
45\
          "time_to_start": "P0Y0M0DT0H57M0S",\
\
46\
          "time_to_start_after_approved": "P0Y0M0DT0H15M0S",\
\
47\
          "real_duration": "P0Y0M0DT7H27M0S"\
\
48\
        },\
\
49\
        "supplier_id": 0,\
\
50\
        "signature_status": "NOT_SIGNED",\
\
51\
        "last_status_change_date": "2020-08-28T09:30:00.000Z",\
\
52\
        "approved_by_id": 0,\
\
53\
        "completed_by_id": 0,\
\
54\
        "started_by_id": 0,\
\
55\
        "paused_by_id": 0,\
\
56\
        "approved_by": "string",\
\
57\
        "completed_by": "string",\
\
58\
        "started_by": "string",\
\
59\
        "paused_by": "string",\
\
60\
        "reported_by": "string",\
\
61\
        "manpower_duration": "P0Y0M0DT7H27M0S",\
\
62\
        "cost_center_id": 0,\
\
63\
        "network_failure_id": 1,\
\
64\
        "created_at": "2019-08-24T14:15:22Z",\
\
65\
        "updated_at": "2019-08-24T14:15:22Z",\
\
66\
        "date_deleted": "2019-08-24T14:15:22Z"\
\
67\
      },\
\
68\
      "relationships": {\
\
69\
        "approvedBy": {\
\
70\
          "data": {\
\
71\
            "type": "operator",\
\
72\
            "id": "string"\
\
73\
          }\
\
74\
        },\
\
75\
        "completedBy": {\
\
76\
          "data": {\
\
77\
            "type": "operator",\
\
78\
            "id": "string"\
\
79\
          }\
\
80\
        },\
\
81\
        "createdBy": {\
\
82\
          "data": {\
\
83\
            "type": "operator",\
\
84\
            "id": "string"\
\
85\
          }\
\
86\
        },\
\
87\
        "files": {\
\
88\
          "data": [\
\
89\
            {\
\
90\
              "type": "file",\
\
91\
              "id": "string"\
\
92\
            }\
\
93\
          ]\
\
94\
        },\
\
95\
        "location": {\
\
96\
          "data": {\
\
97\
            "type": "location",\
\
98\
            "id": "string"\
\
99\
          }\
\
100\
        },\
\
101\
        "operator": {\
\
102\
          "data": {\
\
103\
            "type": "operator",\
\
104\
            "id": "string"\
\
105\
          }\
\
106\
        }\
\
107\
      }\
\
108\
    }\
\
109\
  ],

110
  "included": [\
\
111\
    {\
\
112\
      "id": "string",\
\
113\
      "type": "file",\
\
114\
      "attributes": {\
\
115\
        "file_id": 0,\
\
116\
        "file_uuid": "string",\
\
117\
        "related_to": "BUILDING",\
\
118\
        "related_to_id": 0,\
\
119\
        "related_type": "BUILDING",\
\
120\
        "file_label_id": 0,\
\
121\
        "name": "my_example_file",\
\
122\
        "thumb": "string",\
\
123\
        "file_url": "http://example.com",\
\
124\
        "description": "string",\
\
125\
        "expire_date": "2020-08-28T17:12:00.000Z",\
\
126\
        "has_reminder": true,\
\
127\
        "file_type": "cad",\
\
128\
        "permission_to_technician": true,\
\
129\
        "permission_to_manager": true,\
\
130\
        "permission_to_direct": false,\
\
131\
        "extension": "3gp",\
\
132\
        "network_status": "SHARED",\
\
133\
        "shared_with_supplier": true,\
\
134\
        "shared_with_client": true\
\
135\
      }\
\
136\
    }\
\
137\
  ],

138
  "meta": {

139
    "pagination": {

140
      "total": 1,

141
      "count": 1,

142
      "per_page": 200,

143
      "current_page": 1,

144
      "total_pages": 1

145
    }

146
  },

147
  "links": {

148
    "self": "/path?page=1",

149
    "first": "/path?page=1",

150
    "last": "/path?page=1",

151
    "next": "/path?page=1"

152
  }

153
}
```

[![Infraspeak](https://infraspeak.com/_vercel/image?url=/images/logo.svg&w=1536&q=100)](https://infraspeak.stoplight.io/)

[Home](https://infraspeak.stoplight.io/)

[REST API docs](https://infraspeak.stoplight.io/docs/api)

1\. INTRODUCTION

[Requirements](https://infraspeak.stoplight.io/docs/api/f89e68a07621b-requirements) [Request/Response Format](https://infraspeak.stoplight.io/docs/api/a8b365c9886ae-request-response-format) [HTTP request headers](https://infraspeak.stoplight.io/docs/api/f1c0bb5de545c-http-request-headers) [Parameters](https://infraspeak.stoplight.io/docs/api/1f866ecae49d8-parameters) [Pagination](https://infraspeak.stoplight.io/docs/api/7d56ca7f2fd57-pagination) [Errors](https://infraspeak.stoplight.io/docs/api/be910e4a766ea-errors) [Throttling](https://infraspeak.stoplight.io/docs/api/bb96dca8ef317-throttling)

2\. AUTHENTICATION

[Generating a Token](https://infraspeak.stoplight.io/docs/api/efb05786d9dac-generating-a-token) [Using the Token](https://infraspeak.stoplight.io/docs/api/b12bdbebe6402-using-the-token) [Revoking a Token](https://infraspeak.stoplight.io/docs/api/cb1235a9a476a-revoking-a-token)

3\. WEBHOOKS

[Subscribing](https://infraspeak.stoplight.io/docs/api/469b2f187317d-subscribing-for-webhooks) [Receiving](https://infraspeak.stoplight.io/docs/api/bd5aafb3b7515-receiving-webhooks) [Infraspeak Public REST API](https://infraspeak.stoplight.io/docs/api/dce3ba5e35e9a-infraspeak-public-rest-api)

Buy Orders

Categories

Clients

Contacts

Cost Centers

Elements

Failures

[List all Failures\\
\\
get](https://infraspeak.stoplight.io/docs/api/1405a02f5beb9-list-all-failures) [Create a Failure\\
\\
post](https://infraspeak.stoplight.io/docs/api/5d5fb7b57304c-create-a-failure) [Get a Failure\\
\\
get](https://infraspeak.stoplight.io/docs/api/3ee9f1217376a-get-a-failure) [Delete Failure\\
\\
delete](https://infraspeak.stoplight.io/docs/api/f558bdd898d42-delete-failure) [Update Failure\\
\\
patch](https://infraspeak.stoplight.io/docs/api/ece1fb821e965-update-failure) [List closed Failures\\
\\
get](https://infraspeak.stoplight.io/docs/api/be9dfe304fc53-list-closed-failures) [List open Failures\\
\\
get](https://infraspeak.stoplight.io/docs/api/9a30c0d30d95b-list-open-failures)

Files

Locations

Materials

Operators

Other Costs

Problems

Quotes

Requests

Scheduled Works

Sell Orders

Stock Movements

Stocks

Suppliers

Warehouses

Works

Stock Transactions

Schemas

[Sign in](https://infraspeak.stoplight.io/auth) [powered by **Stoplight**](https://stoplight.io/?utm_source=workspaces&utm_medium=infraspeak&utm_campaign=powered_by&utm_content=/docs/api/1405a02f5beb9-list-all-failures)