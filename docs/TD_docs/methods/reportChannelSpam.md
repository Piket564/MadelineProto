---
title: reportChannelSpam
description: Reports some supergroup channel messages from a user as spam messages
---
## Method: reportChannelSpam  
[Back to methods index](index.md)


YOU CANNOT USE THIS METHOD IN MADELINEPROTO


Reports some supergroup channel messages from a user as spam messages

### Params:

| Name     |    Type       | Required | Description |
|----------|:-------------:|:--------:|------------:|
|channel\_id|[int](../types/int.md) | Yes|Channel identifier|
|user\_id|[int](../types/int.md) | Yes|User identifier|
|message\_ids|Array of [long](../types/long.md) | Yes|Identifiers of messages sent in the supergroup by the user, the list should be non-empty|


### Return type: [Ok](../types/Ok.md)

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

$Ok = $MadelineProto->reportChannelSpam(['channel_id' => int, 'user_id' => int, 'message_ids' => [long], ]);
```

Or, if you're into Lua:

```
Ok = reportChannelSpam({channel_id=int, user_id=int, message_ids={long}, })
```

