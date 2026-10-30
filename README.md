# Support Inbox Auto-Reply (n8n)

An n8n workflow that watches a support inbox and replies automatically to
every new email with a polite acknowledgement.

**Flow:** Gmail Trigger → Gmail (Reply) → Gmail (Add Label)

## Features
- Replies within about a minute of receiving an email
- Ignores no-reply, mailer-daemon and its own messages (no email loops)
- Labels answered emails so each message gets one reply only
- Reply text is easy to edit (see `reply-template.txt`)

## Setup
This repository contains no credentials. After importing the workflow:

1. In n8n choose **Import from file** and select `workflow.json`.
2. Create the Gmail label `auto-replied`.
3. Open each Gmail node and connect your own Google account
   (credential: **Sign in with Google**).
4. Edit the reply text if you want.
5. Click **Execute workflow** to test, then switch the workflow to **Active**.

Never commit passwords, tokens or API keys.

## Customising
- Change the reply in the **Gmail (Reply)** node.
- Change the poll time in the **Gmail Trigger** node.
- Add more sender exclusions in the trigger's search filter.

## Screenshots
![Workflow](screenshots/workflow-canvas.png)
![Successful run](screenshots/successful-run.png)