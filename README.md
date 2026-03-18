# Power-Automate-Task-from-Teams
This is a very simple cloud flow to create To-Do tasks directly from Teams messages. It works for private chats, group chats and channels. You can add your own details to the task but it also saves the context of the task automatically, so you can easily go back to the conversation where the task was assigned to you.

You can trigger this flow directly from Teams, making your work flow easier (no switching between To-Do and Teams!):

<img width="239" alt="image" src="https://github.com/user-attachments/assets/6d54d182-232a-48d7-a063-edb17bfa19d7" />

You can add your own details to the task, such as task title and notes:

<img width="503" alt="image" src="https://github.com/user-attachments/assets/bdcb32c7-a2e6-44cc-8a0a-8896932c9b39" />

The task contais the original context, such as who sent the message, original message content and also a link to the message:

<img width="860" alt="image" src="https://github.com/user-attachments/assets/f361186f-0028-43ac-befc-1c688fd94efe" />


# Flow setup

This is a fairly simple flow. You can find the solution package attached, but to be honest, it is faster to build from scratch. Just refer to the picture below and copypaste the adaptive card code :) 

Tasktitle and notes are coming from the adaptive card.

<img width="600" height="1231" alt="image" src="https://github.com/user-attachments/assets/ac78ff85-b9e0-4c69-b160-c740b23eeb21" />

  
# Adaptive Card

{
    "$schema": "http://adaptivecards.io/schemas/adaptive-card.json",
    "type": "AdaptiveCard",
    "version": "1.3",
    "body": [
        {
            "type": "TextBlock",
            "text": "Task",
            "wrap": true,
            "weight": "Bolder",
            "color": "Accent"
        },
        {
            "type": "Input.Text",
            "id": "tasktitle"
        },
        {
            "type": "TextBlock",
            "text": "Notes",
            "wrap": true,
            "weight": "Bolder",
            "color": "Accent"
        },
        {
            "type": "Input.Text",
            "spacing": "None",
            "id": "notes"
        }
    ],
    "actions": [
        {
            "type": "Action.Submit",
            "title": "Submit"
        }
    ]
}
