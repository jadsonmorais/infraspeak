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

# List all Scheduled Works

get

https://api.infraspeak.com/v3/works/scheduled

Planned Job Orders are referred in Infraspeak's API as Scheduled Works.

This endpoint allows you to fetch all the Scheduled Work (Planned Job Orders).

## [Request](https://infraspeak.stoplight.io/docs/api/e6d6f83217dab-list-all-scheduled-works\#Request)

Security: Bearer Auth

## [Responses](https://infraspeak.stoplight.io/docs/api/e6d6f83217dab-list-all-scheduled-works\#Responses)

200

400

401

404

429

500

OK

### [Body](https://infraspeak.stoplight.io/docs/api/e6d6f83217dab-list-all-scheduled-works\#response-body)

application/json

application/json

data

array\[Scheduled Work\]

id

string

required

ID of the Scheduled Order

Example:

123

type

any

required

Model type

Allowed value:

scheduled\_work

Example:

scheduled\_work

attributes

object

required

relationships

object

The relationships of the Scheduled Work (Only present when expanded in the request)

included

array\[object\]

List of relationships to be included

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

Send API Request

Production

Request Sample: Shell / cURL

```
curl --request GET \

  --url https://api.infraspeak.com/v3/works/scheduled \

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
      "id": "123",\
\
5\
      "type": "scheduled_work",\
\
6\
      "attributes": {\
\
7\
        "entity_id": 123,\
\
8\
        "complete_date": "2014-09-01 02:22:00",\
\
9\
        "cost_center_name": "abc",\
\
10\
        "completed_by_id": 123,\
\
11\
        "completed_percentage": 45,\
\
12\
        "completed_date": "2014-09-01 02:22:00",\
\
13\
        "confirmed": true,\
\
14\
        "failure_id": 0,\
\
15\
        "last_status_change_date": "2014-09-01 02:22:00",\
\
16\
        "last_status_change_operator": "John",\
\
17\
        "manpower_duration": "P0Y0M0DT0H1M19S",\
\
18\
        "manpower_cost": 12.5,\
\
19\
        "observation": "abc",\
\
20\
        "real_start_date": "2014-09-01 02:22:00",\
\
21\
        "running": true,\
\
22\
        "schedule_work_id": 123,\
\
23\
        "signature_status": "NOT_SIGNED",\
\
24\
        "start_date": "2014-09-01 02:22:00",\
\
25\
        "started_by_id": 123,\
\
26\
        "state": "SCHEDULED",\
\
27\
        "time_running": "P0Y0M0DT0H1M19S",\
\
28\
        "visit": 1,\
\
29\
        "work_id": 123,\
\
30\
        "next_sla_date": "2014-09-01 02:22:00",\
\
31\
        "next_sla_percentage": 75.5,\
\
32\
        "next_scheduled_work_sla_id": 123,\
\
33\
        "next_scheduled_work_sla_date": "2014-09-01 02:22:00",\
\
34\
        "next_scheduled_work_sla_status_order": 0,\
\
35\
        "rescheduled_by_user": false,\
\
36\
        "network_id": 123,\
\
37\
        "updated_at": "2014-09-01 02:22:00",\
\
38\
        "display_start_date": "2014-09-01 02:22:00",\
\
39\
        "display_complete_date": "2014-09-01 02:22:00",\
\
40\
        "estimated_duration_absolute_deviation": 150,\
\
41\
        "estimated_duration_relative_deviation": -150\
\
42\
      },\
\
43\
      "relationships": {\
\
44\
        "auditStats": {\
\
45\
          "data": [\
\
46\
            {\
\
47\
              "type": "audit_stats",\
\
48\
              "id": "string"\
\
49\
            }\
\
50\
          ]\
\
51\
        },\
\
52\
        "buyOrders": {\
\
53\
          "data": [\
\
54\
            {\
\
55\
              "type": "buy_order",\
\
56\
              "id": "string"\
\
57\
            }\
\
58\
          ]\
\
59\
        },\
\
60\
        "client": {\
\
61\
          "data": {\
\
62\
            "type": "client",\
\
63\
            "id": "string"\
\
64\
          }\
\
65\
        },\
\
66\
        "completedBy": {\
\
67\
          "data": {\
\
68\
            "type": "operator",\
\
69\
            "id": "string"\
\
70\
          }\
\
71\
        },\
\
72\
        "elementRegistries": {\
\
73\
          "data": [\
\
74\
            {\
\
75\
              "type": "element_registry",\
\
76\
              "id": "string"\
\
77\
            }\
\
78\
          ]\
\
79\
        },\
\
80\
        "entity": {\
\
81\
          "data": {\
\
82\
            "type": "entity",\
\
83\
            "id": "string"\
\
84\
          }\
\
85\
        },\
\
86\
        "events": {\
\
87\
          "data": [\
\
88\
            {\
\
89\
              "type": "event",\
\
90\
              "id": "string"\
\
91\
            }\
\
92\
          ]\
\
93\
        },\
\
94\
        "eventsPlanned": {\
\
95\
          "data": [\
\
96\
            {\
\
97\
              "type": "event",\
\
98\
              "id": "string"\
\
99\
            }\
\
100\
          ]\
\
101\
        },\
\
102\
        "files": {\
\
103\
          "data": [\
\
104\
            {\
\
105\
              "type": "file",\
\
106\
              "id": "string"\
\
107\
            }\
\
108\
          ]\
\
109\
        },\
\
110\
        "gatekeeperAnswerRegistries": {\
\
111\
          "data": [\
\
112\
            {\
\
113\
              "type": "gatekeeper_answer_registry",\
\
114\
              "id": "string"\
\
115\
            }\
\
116\
          ]\
\
117\
        },\
\
118\
        "networkStatus": {\
\
119\
          "data": [\
\
120\
            {\
\
121\
              "type": "SENDER",\
\
122\
              "action": "string",\
\
123\
              "id": "string",\
\
124\
              "in_sync": true,\
\
125\
              "network_entity_uuid": "string",\
\
126\
              "network_relation_id": 0,\
\
127\
              "network_relation_type": "CLIENT",\
\
128\
              "shared": true\
\
129\
            }\
\
130\
          ]\
\
131\
        },\
\
132\
        "otherCosts": {\
\
133\
          "data": [\
\
134\
            {\
\
135\
              "type": "other-cost",\
\
136\
              "id": "string"\
\
137\
            }\
\
138\
          ]\
\
139\
        },\
\
140\
        "participants": {\
\
141\
          "data": [\
\
142\
            {\
\
143\
              "type": "operator",\
\
144\
              "id": "string"\
\
145\
            }\
\
146\
          ]\
\
147\
        },\
\
148\
        "pausedBy": {\
\
149\
          "data": {\
\
150\
            "type": "operator",\
\
151\
            "id": "string"\
\
152\
          }\
\
153\
        },\
\
154\
        "reminderRules": {\
\
155\
          "data": [\
\
156\
            {\
\
157\
              "type": "reminder_rules",\
\
158\
              "id": "string"\
\
159\
            }\
\
160\
          ]\
\
161\
        },\
\
162\
        "reminders": {\
\
163\
          "data": [\
\
164\
            {\
\
165\
              "type": "reminder",\
\
166\
              "id": "string"\
\
167\
            }\
\
168\
          ]\
\
169\
        },\
\
170\
        "requests": {\
\
171\
          "data": [\
\
172\
            {\
\
173\
              "type": "request",\
\
174\
              "id": "string"\
\
175\
            }\
\
176\
          ]\
\
177\
        },\
\
178\
        "scheduledWorkSlas": {\
\
179\
          "data": [\
\
180\
            {\
\
181\
              "type": "schedule_work_sla",\
\
182\
              "id": "string"\
\
183\
            }\
\
184\
          ]\
\
185\
        },\
\
186\
        "startedBy": {\
\
187\
          "data": {\
\
188\
            "type": "operator",\
\
189\
            "id": "string"\
\
190\
          }\
\
191\
        },\
\
192\
        "stock": {\
\
193\
          "data": [\
\
194\
            {\
\
195\
              "type": "stock",\
\
196\
              "id": "string"\
\
197\
            }\
\
198\
          ]\
\
199\
        },\
\
200\
        "stockTasks": {\
\
201\
          "data": [\
\
202\
            {\
\
203\
              "type": "stock",\
\
204\
              "id": "string"\
\
205\
            }\
\
206\
          ]\
\
207\
        },\
\
208\
        "survey": {\
\
209\
          "data": {\
\
210\
            "type": "survey",\
\
211\
            "id": "string"\
\
212\
          }\
\
213\
        },\
\
214\
        "surveyFeedbacks": {\
\
215\
          "data": [\
\
216\
            {\
\
217\
              "type": "survey_feedback",\
\
218\
              "id": "string"\
\
219\
            }\
\
220\
          ]\
\
221\
        },\
\
222\
        "work": {\
\
223\
          "data": {\
\
224\
            "type": "work",\
\
225\
            "id": "string"\
\
226\
          }\
\
227\
        },\
\
228\
        "realStartDateEditedBy": {\
\
229\
          "data": {\
\
230\
            "type": "operator",\
\
231\
            "id": "string"\
\
232\
          }\
\
233\
        },\
\
234\
        "completeDateEditedBy": {\
\
235\
          "data": {\
\
236\
            "type": "operator",\
\
237\
            "id": "string"\
\
238\
          }\
\
239\
        },\
\
240\
        "failureScheduleMapping": {\
\
241\
          "data": [\
\
242\
            {\
\
243\
              "type": "failure_schedule_mapping",\
\
244\
              "id": "string"\
\
245\
            }\
\
246\
          ]\
\
247\
        }\
\
248\
      }\
\
249\
    }\
\
250\
  ],

251
  "included": [\
\
252\
    {}\
\
253\
  ],

254
  "meta": {

255
    "pagination": {

256
      "total": 1,

257
      "count": 1,

258
      "per_page": 200,

259
      "current_page": 1,

260
      "total_pages": 1

261
    }

262
  },

263
  "links": {

264
    "self": "/path?page=1",

265
    "first": "/path?page=1",

266
    "last": "/path?page=1",

267
    "next": "/path?page=1"

268
  }

269
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

Files

Locations

Materials

Operators

Other Costs

Problems

Quotes

Requests

Scheduled Works

[List all Scheduled Works\\
\\
get](https://infraspeak.stoplight.io/docs/api/e6d6f83217dab-list-all-scheduled-works) [Get a Scheduled Work\\
\\
get](https://infraspeak.stoplight.io/docs/api/6d4bdf51c7f0d-get-a-scheduled-work) [Update a Scheduled Work\\
\\
patch](https://infraspeak.stoplight.io/docs/api/eba367896961b-update-a-scheduled-work)

Sell Orders

Stock Movements

Stocks

Suppliers

Warehouses

Works

Stock Transactions

Schemas

[Sign in](https://infraspeak.stoplight.io/auth) [powered by **Stoplight**](https://stoplight.io/?utm_source=workspaces&utm_medium=infraspeak&utm_campaign=powered_by&utm_content=/docs/api/e6d6f83217dab-list-all-scheduled-works)