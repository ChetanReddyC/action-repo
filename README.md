# action-repo

This repository is used to trigger GitHub webhooks for Push, Pull Request, and Merge events.

## Webhook Configuration

To set up the webhook pointing to your webhook receiver:

1. Go to this repo's **Settings** → **Webhooks** → **Add webhook**

2. Configure:
   - **Payload URL:** `https://<your-ngrok-url>/webhook/receiver`
   - **Content type:** `application/json`
   - **Secret:** *(leave blank for testing)*
   - **Which events?** Select:
     - ✅ Pushes
     - ✅ Pull requests

3. Click **Add webhook**

## Testing

After webhook is configured:

- **Push:** Commit and push any change to this repo
- **Pull Request:** Create a new PR from a feature branch
- **Merge:** Merge a PR to trigger merge event

Events will appear in the dashboard: `http://localhost:5000` (or your ngrok URL)
