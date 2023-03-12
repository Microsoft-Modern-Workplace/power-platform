---
title: "Download chatbot sessions in Microsoft Teams"
description: "Download Power Virtual Agents chatbot session information from the last 30 days in the app in Microsoft Teams."
keywords: "PVA, Teams"

---

# Analyze session information in the Power Virtual Agents app in Microsoft Teams

Select the version of Power Virtual Agents you're using here:

> [!div class="op_single_selector"]
>
> - [Power Virtual Agents web app](../analytics-sessions.md)
> - [Power Virtual Agents app in Microsoft Teams](analytics-sessions-teams.md)

By default, you can download up to seven days of bot conversation transcript sessions from the past 30 days directly from the Power Virtual Agents app in Microsoft Teams.

> [!NOTE]
> If you no longer have access to your environment, you'll need to [create a support request](https://admin.powerplatform.microsoft.com/support) in the Power Platform admin center.

## Prerequisites

- [Learn more about what you can do with Power Virtual Agents](fundamentals-what-is-power-virtual-agents-teams.md).

## Download session transcript information from the Power Virtual Agents app in Teams

1. In the navigation menu, select **Analytics** and go to the **Sessions** tab.

    If your bot had a high number of sessions, they'll be broken down into multiple rows. Each row contains 2500 sessions.

1. Select each row to download the session transcripts for the specified time frame.

    :::image type="content" source="../media/analytics-sessions/analytics-sessions-billing-teams.png" alt-text="Screenshot of the sessions download page in the Power Virtual Agents app in Teams.":::

> [!NOTE]
> You need to have sufficient permissions to download sessions. If you're using the Power Virtual Agents app in Teams, you need to be the **Team Owner**.

The downloaded file contains the following information:

- SessionID: A unique identifier per session.

- StartDateTime: Time at which the session started. Entries are sorted by this column in descending order.

- InitialUserMessage: First message typed by the user.

- TopicName: Name of the last authored topic that was triggered in this session.

- ChatTranscript: Transcript of the session in the following format, `User says: <message-text>; Bot says: <message-text>;`.
  - Conversation turns are separated by semicolons
  - _Bot says_ doesn't include the options presented to the user.

    Example:

    ```text
    User says: store hours; Bot says: Which store are you asking about?; User says: Bellevue; Bot says: Bellevue store is open from 10am to 7pm every day.;
    ```

- SessionOutcome: Outcome of the session (Resolved, Escalated, Abandoned, Unengaged).

- TopicId: A unique identifier of the last authored topic triggered in this session.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
