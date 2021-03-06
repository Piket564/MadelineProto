---
title: getSupportUser
description: Returns user that can be contacted to get support
---
## Method: getSupportUser  
[Back to methods index](index.md)


YOU CANNOT USE THIS METHOD IN MADELINEPROTO


Returns user that can be contacted to get support

### Params:

| Name     |    Type       | Required | Description |
|----------|:-------------:|:--------:|------------:|


### Return type: [User](../types/User.md)

### Example:


```
$MadelineProto = new \danog\MadelineProto\API();
if (isset($token)) { // Login as a bot
    $this->bot_login($token);
}
if (isset($number)) { // Login as a user
    $sentCode = $MadelineProto->phone_login($number);
    echo 'Enter the code you received: ';
    $code = '';
    for ($x = 0; $x < $sentCode['type']['length']; $x++) {
        $code .= fgetc(STDIN);
    }
    $MadelineProto->complete_phone_login($code);
}

$User = $MadelineProto->getSupportUser();
```

Or, if you're into Lua:

```
User = getSupportUser({})
```

