# register_device


Registers a new device to the Apple Dev Portal




> This will register an iOS device with the Developer Portal so that you can include it in your provisioning profiles.
This is an optimistic action, in that it will only ever add a device to the member center. If the device has already been registered within the member center, it will be left alone in the member center.
The action will connect to the Apple Developer Portal using the username you specified in your `Appfile` with `apple_id`, but you can override it using the `username` option.


register_device |
-----|----
Supported platforms | ios
Author | @pvinis



**2 Examples**

```ruby
register_device(
  name: "Luka iPhone 6",
  udid: "1234567890123456789012345678901234567890"
) # Simply provide the name and udid of the device
```

```ruby
register_device(
  name: "Luka iPhone 6",
  udid: "1234567890123456789012345678901234567890",
  team_id: "XXXXXXXXXX",         # Optional, if you"re a member of multiple teams, then you need to pass the team ID here.
  username: "luka@goonbee.com"   # Optional, lets you override the Apple Member Center username.
)
```





**Parameters**

Key | Description
----|------------
  `name` | Provide the name of the device to register as
  `udid` | Provide the UDID of the device to register as
  `team_id` | The ID of your Developer Portal team if you're in multiple teams
  `team_name` | The name of your Developer Portal team if you're in multiple teams
  `username` | Optional: Your Apple ID




<hr />
To show the documentation in your terminal, run
```no-highlight
fastlane action register_device
```

<a href="https://github.com/fastlane/fastlane/blob/master/fastlane/lib/fastlane/actions/register_device.rb" target="_blank">View source code</a>

<hr />

<a href="/actions"><b>Back to actions</b></a>
