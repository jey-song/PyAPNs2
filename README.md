# PyAPNs2
Python library for interacting with the Apple Push Notification service (APNs) via HTTP/2 protocol

## Installation

Either download the source from GitHub or use easy_install:

    $ easy_install apns2

## Sample usage

```python
from apns2.client import APNsClient
from apns2.payload import Payload

token_hex = 'bb1ee6479f2954d43bfb7e857d69a31296ff7c86670bd9b39ad8102638e9709d'
payload = Payload(alert="Hello World!", sound="default", badge=1, mutable_content=True, ext={"t":"","url":"www.baidu.com"})
client = APNsClient('key.pem', use_sandbox=True)
client.send_notification(token_hex, payload, topic='com.xxx.xxx')
```

## Further Info

[iOS Reference Library: Local and Push Notification Programming Guide][a1]

## License

PyAPNs2 is distributed under the terms of the MIT license.

See [LICENSE](LICENSE) file for the complete license details.

[a1]:https://developer.apple.com/library/ios/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/Chapters/Introduction.html
