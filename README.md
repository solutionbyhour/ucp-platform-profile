# UCP platform profile — checkout-conform

Public [UCP](https://ucp.dev) platform profile for **checkout-conform**, a conformance
tester for agentic checkout (UCP / ACP) built by SolutionByHour.

UCP merchants download the profile URI an agent sends in `UCP-Agent` /
`meta.ucp-agent.profile` to identify the caller and negotiate capabilities.

Use the **jsDelivr** URL for a published version (tags are immutable):

    https://cdn.jsdelivr.net/gh/solutionbyhour/ucp-platform-profile@v1/platform.json

jsDelivr serves `application/json` with `Cache-Control: public, …`, which UCP merchants
require. GitHub Pages sends `max-age` without `public`, and Shopify rejects it
("Invalid cache control").

Edit and publish new versions from the checkout-conform UI (Platform profile), or
regenerate with `conform profile [fragment.json] > platform.json`.
