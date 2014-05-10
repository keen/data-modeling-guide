Data Modeling for Games
=======================

### New User Registration

```
create_account = {
  "user": {
    "email": "michelle@keen.io",
    "id" : "92379hasdbc9377435",
    "referral" : "web signup",
    "city": "San Francisco",
    "state": "California"
  }
}
```


### In-Game Activities

**Examples:** Starting a new level, playing a turn, winning/losing a battle, completing a tutorial.

```
level_start = {
  "player": {
    "email": "michelle@keen.io",
    "id" : "92379hasdbc9377435"
  },
  "level" : 3,
  "session": {
    "time_in_game": 23453465
  },
  "device": {
    "deviceID": "2983748309240384",
    "deviceFamily": "Galaxy S3""
  }
}
```

```
play = {
  "user" : {
    "email": "michelle@keen.io",
    "id" : "92379hasdbc9377435"
  },
  "device": {
	"deviceID": "2983748309240384",
    "deviceFamily": "Galaxy S3""
  },
  "level" : 3,
  "version": "3.4.1"
}
```


### In-App Purchases

```
purchase = {
  "user": {
    "email": "michelle@keen.io",
    "id" : "92379hasdbc9377435"
  },
  "amount_USD_cents" : 800,
  "item" : "enchanted catnip"
}
```


### Game Downloads

```
game_download = {
  "user": {
    "email": "michelle@keen.io",
    "id" : "92379hasdbc9377435"
  },
  "game": {
    "name": "Jumpy Cats",
    "version": "3.0.1",
    "developer": "HyperLabs",
    "publisher": "HyperLabs",
    "rating": 4.3,
    "category": "RPG",
    "genre": ["Simulation", "Educational", "Cats"]
  }
}
```


### Game Submissions

```
game_submission = {
  "user": {
    "email": "charlie@hyperlabs.co",
    "id" : "434251252ffd3h234f"
  },
  "game": {
    "name": "Jumpy Cats 2: Boats vs. Cats",
    "version": "1.2",
    "developer": "HyperLabs",
    "publisher": "HyperLabs",
    "rating": 5.0,
    "category": "Experience",
    "genre": ["Simulation", "Horror", "Cats", "Boats"]
  }
}
```
