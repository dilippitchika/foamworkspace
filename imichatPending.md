# All items pending across the bot chat integration

## Missing templates

1. ABC
   1. List - Scheduled for hip
   2. Time
   3. Rich links
   4. Text with attachments - scheduled for hip
2. Whatsapp
   1. Attachments - scheduled for hip
3. Livechat
   1. Attachments - scheduled for hip

## Storing pre-chat variables in bot

1. Which ones are customer variables and won't be changing?
2. Which are message/chat level variables? -> Given that they are specific to chat how will we store them? - **Given that our customer creation is at a chat_id level it's better if we store this in consumer extra params**

## Markdown support

1. Is anything special needed to build support for markdown from the backend? - Not needed - only needed via frontend
2. Prevent and sanitize certain html tags - https://weblog.west-wind.com/posts/2018/Aug/31/Markdown-and-Cross-Site-Scripting (for .NET)
3. We only use <br> but remaining should just come via markdown - like italicise, bold etc.

## Agent handover

### For Q&A bots

Today if we want to do dynamic agent handover for Q&A bots, we need to have a way to send certain details at an article level to IMIchat.

Representative flow-

1. User talks to bot -> Bot answers certain questions related to a category and either the user or the bot understands that there is a need for agent handover -> Requests handover on the basis of a particular logic.
   1. Should be able to define their own handover parameters
   2. Should be ideally done once and applied for all
