---
title: editMessageCaption
description: Edits message content caption. Non-bots can edit message in a limited period of time. Returns edited message after edit is complete server side
---
## Method: editMessageCaption  
[Back to methods index](index.md)


YOU CANNOT USE THIS METHOD IN MADELINEPROTO


Edits message content caption. Non-bots can edit message in a limited period of time. Returns edited message after edit is complete server side

### Params:

| Name     |    Type       | Required | Description |
|----------|:-------------:|:--------:|------------:|
|chat\_id|[InputPeer](../types/InputPeer.md) | Yes|Chat the message belongs to|
|message\_id|[long](../types/long.md) | Yes|Identifier of the message|
|reply\_markup|[ReplyMarkup](../types/ReplyMarkup.md) | Yes|Bots only. New message reply markup|
|caption|[string](../types/string.md) | Yes|New message content caption, 0-200 characters|


### Return type: [Message](../types/Message.md)

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

$Message = $MadelineProto->editMessageCaption(['chat_id' => InputPeer, 'message_id' => long, 'reply_markup' => ReplyMarkup, 'caption' => string, ]);
```

Or, if you're into Lua:

```
Message = editMessageCaption({chat_id=InputPeer, message_id=long, reply_markup=ReplyMarkup, caption=string, })
```


## Usage of reply_markup

You can provide bot API reply_markup objects here.  


