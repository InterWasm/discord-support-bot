# Discord Support bot

There are 2 roles for the support system.

- Admins
- Experts

Admins can issue commands below in **admin-bot** channel to do operations on experts.

| Commands                          | Description                                                                         |
|-----------------------------------|-------------------------------------------------------------------------------------|
| !listExperts                      | Lists all the experts                                                               |
| !addExpert @user :selected_emoji: | Adds an expert to the list. Used with 2 parameters.<br>User and the selected emoji. |
| !removeExpert @user               | Removes an expert from the list. Used with 1<br>parameter. The user.                |

![List experts](assets/list-experts.png)
![Remove expert](assets/remove-expert.png)
![Add expert](assets/add-expert.png)

In order for an expert to be added to the list, first they need to be added to the **expert** role in the server.
After adding them, they need to be in the **admin-bot** channel to be added/removed to the expert
list.
# Workflow

In the monitored channels (**test-bot** for our case), people can react to a message with a question mark emoji (❓) to mark it as a question.

![Marking question](assets/question.png)

The bot then sends the tagged message to our expert channel (**support-bot**).

![Ticket](assets/ticket.png)

This tagged message can also be viewed in the **Pinned Messages** until it's closed.

![Pinned ticket](assets/ticket-pinned.png)

When an expert or admin wants to assign the ticket to an expert, all they have to do is react to that ticket with the expert's selected emoji.

![Assigned ticket](assets/ticket-assigned.png)

Experts can view their assigned tickets in the private channel named after them at the end of discord channels.

![Private expert channels](assets/private-expert-channels.png)

When the title of the ticket is clicked, it navigates to the original message for the expert to answer.

When the expert and the user are happy with the question/answer, the ticket can be closed either
reacting the original message or the ticket in the expert channels with an exclamation mark emoji (❗)

![Closed question](assets/question-closed.png)
![Closed ticket](assets/ticket-closed.png)

When a ticket is closed, it's automatically removed from the **Pinned Messages**.