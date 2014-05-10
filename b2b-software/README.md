Data Modeling for SaaS/B2B Apps
===============================

### New User Registration

```
create_account = {
  "user": {
    "email": "timmy@coolstuff.co",
    "id" : "92379hasdbc9377435",
    "title" : "Boss",
    "company" : "Cool Stuff, Inc.",
    "type" : "referral"
  }
}
```

### Logins

```
user_login = {
  "user": {
    "email": "timmy@coolstuff.co",
    "id" : "92379hasdbc9377435"
  }
}
```


### Arbitrary Object Creation

```
new_project_created = {
  "user": {
    "email": "timmy@coolstuff.co",
    "id" : "92379hasdbc9377435"
  },
  "project": {
    "name": "Cool Stuff Workspace",
    "id" : "59710943579102375"
  }
}
```

```
job_application = {
  "user": {
    "email": "timmy@coolstuff.co",
    "id" : "92379hasdbc9377435",
    "title" : "Boss",
    "company" : "Cool Stuff, Inc.",
    "type" : "referral"
  },
  "job" : {
    "id": "29387487273",
    "description": "IT Manager, Regional User Support",
    "company": "Better Co.",
    "location": {
      "city" : "Mountain View",
      "country" : "US",
      "state" : "CA"
    }
  }
}
```



### Upgrades

```
account_change = {
  "user": {
    "email": "timmy@coolstuff.co",
    "id" : "92379hasdbc9377435",
    "title" : "Boss",
    "company" : "Cool Stuff, Inc.",
    "type" : "referral"
  },
  "switch_from": "free",
  "switch_to": "pro",
  "monthly_rate_cents": 5000
}
```

### Purchases

```
purchase = {
  "item": "sophisticated orange turtleneck with deer on it",
  "cost": 469.50,
  "payment_method": "Bank Simple VISA",
  "customer": {
    "id": 233255,
    "name": "Francis Woodbury",
    "age": 28,
    "address": {
      "city": "San Francisco",
      "country": "USA"
    }
  }
}
```


### User Invites

```
new_invitation_sent = {
  "sender": {
    "email": "timmy@coolstuff.co",
    "id" : "92379hasdbc9377435",
    "title" : "Boss",
    "company" : "Cool Stuff, Inc.",
    "type" : "referral"
  },
  "recipient": {
    "email": "jimmy@coolstuff.co",
    "title" : "IT Manager",
    "company" : "Cool Stuff, Inc."
  }
}
```