---
title: requestAuthPasswordRecovery
description: Requests to send password recovery code to email. Works only when authGetState returns authStateWaitPassword. Returns authStateWaitPassword on success
---
## Method: requestAuthPasswordRecovery  
[Back to methods index](index.md)


YOU CANNOT USE THIS METHOD IN MADELINEPROTO


Requests to send password recovery code to email. Works only when authGetState returns authStateWaitPassword. Returns authStateWaitPassword on success

### Params:

| Name     |    Type       | Required | Description |
|----------|:-------------:|:--------:|------------:|


### Return type: [AuthState](../types/AuthState.md)

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

$AuthState = $MadelineProto->requestAuthPasswordRecovery();
```

Or, if you're into Lua:

```
AuthState = requestAuthPasswordRecovery({})
```

