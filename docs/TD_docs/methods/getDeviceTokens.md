---
title: getDeviceTokens
description: Returns list of used device tokens
---
## Method: getDeviceTokens  
[Back to methods index](index.md)


YOU CANNOT USE THIS METHOD IN MADELINEPROTO


Returns list of used device tokens

### Params:

| Name     |    Type       | Required | Description |
|----------|:-------------:|:--------:|------------:|


### Return type: [DeviceTokenSet](../types/DeviceTokenSet.md)

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

$DeviceTokenSet = $MadelineProto->getDeviceTokens();
```

Or, if you're into Lua:

```
DeviceTokenSet = getDeviceTokens({})
```

