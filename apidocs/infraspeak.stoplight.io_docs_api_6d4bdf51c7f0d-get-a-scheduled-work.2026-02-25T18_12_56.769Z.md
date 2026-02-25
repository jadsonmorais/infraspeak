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

# Get a Scheduled Work

get

https://api.infraspeak.com/v3/works/scheduled/{scheduledWorkId}

Planned Job Orders are referred in Infraspeak's API as Scheduled Works.

This endpoint allows you to get information about a specific Scheduled Work (Planned Job Order).

## [Request](https://infraspeak.stoplight.io/docs/api/6d4bdf51c7f0d-get-a-scheduled-work\#Request)

Security: Bearer Auth

### [Path Parameters](https://infraspeak.stoplight.io/docs/api/6d4bdf51c7f0d-get-a-scheduled-work\#Path-Parameters)

scheduledWorkId

string

required

The Schedule Work ID

## [Responses](https://infraspeak.stoplight.io/docs/api/6d4bdf51c7f0d-get-a-scheduled-work\#Responses)

200

400

401

404

429

500

OK

### [Body](https://infraspeak.stoplight.io/docs/api/6d4bdf51c7f0d-get-a-scheduled-work\#response-body)

application/json

application/json

data

Scheduled Work

Scheduled Order model structure details

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

Auth

Token:

Parameters

scheduledWorkId\*:

Send API Request

Production

Request Sample: Shell / cURL

```
curl --request GET \

  --url https://api.infraspeak.com/v3/works/scheduled/{scheduledWorkId} \

  --header 'Accept: application/json' \

  --header 'Authorization: Bearer 123'
```

Response Example

```
1
{

2
  "data": {

3
    "id": "123",

4
    "type": "scheduled_work",

5
    "attributes": {

6
      "entity_id": 123,

7
      "complete_date": "2014-09-01 02:22:00",

8
      "cost_center_name": "abc",

9
      "completed_by_id": 123,

10
      "completed_percentage": 45,

11
      "completed_date": "2014-09-01 02:22:00",

12
      "confirmed": true,

13
      "failure_id": 0,

14
      "last_status_change_date": "2014-09-01 02:22:00",

15
      "last_status_change_operator": "John",

16
      "manpower_duration": "P0Y0M0DT0H1M19S",

17
      "manpower_cost": 12.5,

18
      "observation": "abc",

19
      "real_start_date": "2014-09-01 02:22:00",

20
      "running": true,

21
      "schedule_work_id": 123,

22
      "signature_status": "NOT_SIGNED",

23
      "start_date": "2014-09-01 02:22:00",

24
      "started_by_id": 123,

25
      "state": "SCHEDULED",

26
      "time_running": "P0Y0M0DT0H1M19S",

27
      "visit": 1,

28
      "work_id": 123,

29
      "next_sla_date": "2014-09-01 02:22:00",

30
      "next_sla_percentage": 75.5,

31
      "next_scheduled_work_sla_id": 123,

32
      "next_scheduled_work_sla_date": "2014-09-01 02:22:00",

33
      "next_scheduled_work_sla_status_order": 0,

34
      "rescheduled_by_user": false,

35
      "network_id": 123,

36
      "updated_at": "2014-09-01 02:22:00",

37
      "display_start_date": "2014-09-01 02:22:00",

38
      "display_complete_date": "2014-09-01 02:22:00",

39
      "estimated_duration_absolute_deviation": 150,

40
      "estimated_duration_relative_deviation": -150

41
    },

42
    "relationships": {

43
      "auditStats": {

44
        "data": [\
\
45\
          {\
\
46\
            "type": "audit_stats",\
\
47\
            "id": "string"\
\
48\
          }\
\
49\
        ]

50
      },

51
      "buyOrders": {

52
        "data": [\
\
53\
          {\
\
54\
            "type": "buy_order",\
\
55\
            "id": "string"\
\
56\
          }\
\
57\
        ]

58
      },

59
      "client": {

60
        "data": {

61
          "type": "client",

62
          "id": "string"

63
        }

64
      },

65
      "completedBy": {

66
        "data": {

67
          "type": "operator",

68
          "id": "string"

69
        }

70
      },

71
      "elementRegistries": {

72
        "data": [\
\
73\
          {\
\
74\
            "type": "element_registry",\
\
75\
            "id": "string"\
\
76\
          }\
\
77\
        ]

78
      },

79
      "entity": {

80
        "data": {

81
          "type": "entity",

82
          "id": "string"

83
        }

84
      },

85
      "events": {

86
        "data": [\
\
87\
          {\
\
88\
            "type": "event",\
\
89\
            "id": "string"\
\
90\
          }\
\
91\
        ]

92
      },

93
      "eventsPlanned": {

94
        "data": [\
\
95\
          {\
\
96\
            "type": "event",\
\
97\
            "id": "string"\
\
98\
          }\
\
99\
        ]

100
      },

101
      "files": {

102
        "data": [\
\
103\
          {\
\
104\
            "type": "file",\
\
105\
            "id": "string"\
\
106\
          }\
\
107\
        ]

108
      },

109
      "gatekeeperAnswerRegistries": {

110
        "data": [\
\
111\
          {\
\
112\
            "type": "gatekeeper_answer_registry",\
\
113\
            "id": "string"\
\
114\
          }\
\
115\
        ]

116
      },

117
      "networkStatus": {

118
        "data": [\
\
119\
          {\
\
120\
            "type": "SENDER",\
\
121\
            "action": "string",\
\
122\
            "id": "string",\
\
123\
            "in_sync": true,\
\
124\
            "network_entity_uuid": "string",\
\
125\
            "network_relation_id": 0,\
\
126\
            "network_relation_type": "CLIENT",\
\
127\
            "shared": true\
\
128\
          }\
\
129\
        ]

130
      },

131
      "otherCosts": {

132
        "data": [\
\
133\
          {\
\
134\
            "type": "other-cost",\
\
135\
            "id": "string"\
\
136\
          }\
\
137\
        ]

138
      },

139
      "participants": {

140
        "data": [\
\
141\
          {\
\
142\
            "type": "operator",\
\
143\
            "id": "string"\
\
144\
          }\
\
145\
        ]

146
      },

147
      "pausedBy": {

148
        "data": {

149
          "type": "operator",

150
          "id": "string"

151
        }

152
      },

153
      "reminderRules": {

154
        "data": [\
\
155\
          {\
\
156\
            "type": "reminder_rules",\
\
157\
            "id": "string"\
\
158\
          }\
\
159\
        ]

160
      },

161
      "reminders": {

162
        "data": [\
\
163\
          {\
\
164\
            "type": "reminder",\
\
165\
            "id": "string"\
\
166\
          }\
\
167\
        ]

168
      },

169
      "requests": {

170
        "data": [\
\
171\
          {\
\
172\
            "type": "request",\
\
173\
            "id": "string"\
\
174\
          }\
\
175\
        ]

176
      },

177
      "scheduledWorkSlas": {

178
        "data": [\
\
179\
          {\
\
180\
            "type": "schedule_work_sla",\
\
181\
            "id": "string"\
\
182\
          }\
\
183\
        ]

184
      },

185
      "startedBy": {

186
        "data": {

187
          "type": "operator",

188
          "id": "string"

189
        }

190
      },

191
      "stock": {

192
        "data": [\
\
193\
          {\
\
194\
            "type": "stock",\
\
195\
            "id": "string"\
\
196\
          }\
\
197\
        ]

198
      },

199
      "stockTasks": {

200
        "data": [\
\
201\
          {\
\
202\
            "type": "stock",\
\
203\
            "id": "string"\
\
204\
          }\
\
205\
        ]

206
      },

207
      "survey": {

208
        "data": {

209
          "type": "survey",

210
          "id": "string"

211
        }

212
      },

213
      "surveyFeedbacks": {

214
        "data": [\
\
215\
          {\
\
216\
            "type": "survey_feedback",\
\
217\
            "id": "string"\
\
218\
          }\
\
219\
        ]

220
      },

221
      "work": {

222
        "data": {

223
          "type": "work",

224
          "id": "string"

225
        }

226
      },

227
      "realStartDateEditedBy": {

228
        "data": {

229
          "type": "operator",

230
          "id": "string"

231
        }

232
      },

233
      "completeDateEditedBy": {

234
        "data": {

235
          "type": "operator",

236
          "id": "string"

237
        }

238
      },

239
      "failureScheduleMapping": {

240
        "data": [\
\
241\
          {\
\
242\
            "type": "failure_schedule_mapping",\
\
243\
            "id": "string"\
\
244\
          }\
\
245\
        ]

246
      }

247
    }

248
  },

249
  "included": [\
\
250\
    {}\
\
251\
  ]

252
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

[Sign in](https://infraspeak.stoplight.io/auth) [powered by **Stoplight**](https://stoplight.io/?utm_source=workspaces&utm_medium=infraspeak&utm_campaign=powered_by&utm_content=/docs/api/6d4bdf51c7f0d-get-a-scheduled-work)