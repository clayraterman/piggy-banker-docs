# Source: https://docs.cfo.ai/automation/triggers

A **Trigger** is a saved instruction Ari runs by itself on a schedule, like a weekly variance summary sent to you every Monday morning, without you needing to ask each time.

## 

[​](https://docs.cfo.ai/automation/triggers#create-a-trigger)

Create a Trigger

Ask Ari to schedule one, giving it:

- **A name** you’ll recognize later.
- **A prompt** — phrased as a normal request, since it runs unattended and has to stand on its own without the rest of your conversation for context.
- **A schedule**, including your timezone when you specify a local time. Ari converts it to the schedule format it stores internally.
- **A delivery destination**: your Slack direct messages or your verified email address. Ari asks you to choose before it creates or updates a Trigger.

A Trigger starts enabled as soon as you create it.

Trigger schedules use a fixed UTC time. A Trigger set for a particular local time may shift by an hour when daylight saving time changes.

## 

[​](https://docs.cfo.ai/automation/triggers#pause-resume-or-change-a-trigger)

Pause, resume, or change a Trigger

Ask Ari to list your Triggers, then:

- **Pause** one without deleting it, and **resume** it later.
- **Update** its name, prompt, or schedule.
- **Delete** it once you no longer need it.

You can only see and manage your own Triggers, not another workspace member’s.

## 

[​](https://docs.cfo.ai/automation/triggers#what-makes-a-good-trigger-prompt)

What makes a good Trigger prompt

Because a Trigger fires with no conversation around it, write the prompt as if you were asking Ari cold: name the Table Block, Page, or Variable involved, and be specific about what you want back, like “Summarize the variance between Actuals and Forecast for Operating Expense over the last closed month, flag anything over 10%, and send the summary to my Slack direct messages.” Ari can deliver results only to your own Slack direct messages or verified email. It cannot post a scheduled update to a shared Slack channel or message another person. It also cannot complete work that requires your approval during the run, such as merging or deleting a Scenario.

## 

[​](https://docs.cfo.ai/automation/triggers#related)

Related

- [Save a workflow as a Skill](https://docs.cfo.ai/automation/skills)
- [Interactive Guides](https://docs.cfo.ai/automation/guides)

Ctrl+I