---
title: deleteMessagesFromUser
description: Deletes all messages in the chat sent by the specified user. Works only in supergroup channel chats, needs appropriate privileges
---
## Method: deleteMessagesFromUser  
[Back to methods index](index.md)


YOU CANNOT USE THIS METHOD IN MADELINEPROTO


Deletes all messages in the chat sent by the specified user. Works only in supergroup channel chats, needs appropriate privileges

### Params:

| Name     |    Type       | Required | Description |
|----------|:-------------:|:--------:|------------:|
|chat\_id|[InputPeer](../types/InputPeer.md) | Yes|Chat identifier|
|user\_id|[int](../types/int.md) | Yes|User identifier|


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

$Ok = $MadelineProto->deleteMessagesFromUser(['chat_id' => InputPeer, 'user_id' => int, ]);
```

Or, if you're into Lua:

```
Ok = deleteMessagesFromUser({chat_id=InputPeer, user_id=int, })
```

