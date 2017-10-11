# testAutomationHackaton
Preparation for Test Automation Hackaton
This is REST API server for storing/managing TestUsers. DynamoDB NOSQL used to store data.

endpoint:
https://ch7n1tyg3g.execute-api.eu-central-1.amazonaws.com/prod

create new TestUser with data and status
POST https://ch7n1tyg3g.execute-api.eu-central-1.amazonaws.com/prod
{
  "id": "242423234234",
  "firstname": "TestName",
  "lastname": "TestName",
  "userstatus": "NEW",
  "extdata": "{\"anydatakey\":\"anydatavalue\"}"
}

modify TestUser
PUT https://ch7n1tyg3g.execute-api.eu-central-1.amazonaws.com/prod
{
  "id": "242423234234",
  "firstname": "TestNameChanged",
  "lastname": "TestNameChanged",
  "userstatus": "CHANGED",
  "extdata": "{\"anydatakey\":\"anydatavaluechanged\"}",
  "modificationdate": 1111111111111
}

get all TestUsers
GET https://ch7n1tyg3g.execute-api.eu-central-1.amazonaws.com/prod

get TestUser by id
GET https://ch7n1tyg3g.execute-api.eu-central-1.amazonaws.com/prod/{id}

delete TestUser by id
DELETE https://ch7n1tyg3g.execute-api.eu-central-1.amazonaws.com/prod
{
	"id": "242423234234"
}


get latest user by status
GET https://ch7n1tyg3g.execute-api.eu-central-1.amazonaws.com/prod/status/{status}
