
# slack-csharp

This [SDK](https://github.com/sdk-fabric/slack-csharp) is managed by the [SDK Fabric](https://sdk-fabric.org/) project, a global infrastructure to
automatically generate SDKs for every API.

You can find more information about this SDK at [TypeHub](https://typehub.cloud/):
https://app.typehub.cloud/d/sdkfabric/slack

## Usage

```csharp
using SdkFabric.Slack.Client;

Client client = Client.Build("[access_token]")

// Deletes a message from a channel.
Delete_Message_Response response = client.Chat().delete(new Delete_Message_Request());

// Retrieves a permalink URL for a specific existing message.
Get_Permalink_Response response = client.Chat().getPermalink("channel", "message_ts");

// Sends an ephemeral message to a user in a channel.
Post_Ephemeral_Response response = client.Chat().postEphemeral(new Post_Ephemeral_Request());

// Sends a message to a channel.
Post_Message_Response response = client.Chat().postMessage(new Post_Message_Request());

// Schedules a message to be sent to a channel at a future time.
Schedule_Message_Response response = client.Chat().scheduleMessage(new Schedule_Message_Request());

// Updates a message in a channel.
Update_Message_Response response = client.Chat().update(new Update_Message_Request());
```
