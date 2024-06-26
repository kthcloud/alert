# 📣 kthcloud/console-alert
Alert provider for kthcloud services

## Configuration
The console fetches the alert.json file upon load, and displays any alerts there based on the configuration below:

```json5
{
    "alerts": [
        {
            
            // Set the content
            "title": "This is an alert",
            "content": "", // optional

            // Show only on certain pages or domains
            "domains": ["cloud.cbh.kth.se", "beta.app.cloud.cbh.kth.se", "localhost:3000"], // optional, default everywhere
            "pages": ["/", "/deploy", "/edit"], // optional, default "/deploy"

            // Will add a button to the alert
            "link": "https://www.kth.se", // optional, default none

            // Decide when to show the alert
            "showFrom": "1970-01-01T00:00:00Z", // optional, default always
            "showUntil": "1970-01-01T00:00:00Z", // optional, default always

            // Set the severity (color and icon) of the alert
            // Choose from: success, info, warning, error
            "severity": "error", // optional, default info. 
            
            // Variant of alert bar
            // Choose from: filled, outlined, (when not set it has the background color of outlined but no borders)
            "variant": "outlined", // optional, default is the "not set" above

            // Active
            "active": true // optional, default true
        }
    ]
}
```
