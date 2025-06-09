# LowValueMeetingDecider
Agentic Zapier workflow to decide meeting importance

Here's a detailed README description for your Zapier-based agentic workflow:

---

# 📅 Smart Meeting Evaluator – Zapier Agentic Workflow

This Zapier Agentic Workflow intelligently evaluates calendar events and helps optimize your time by automatically analyzing the **usefulness of meetings**, providing a **Slack-based decision flow**, and even **removing low-value events** from your schedule.

---

## 🧠 What It Does

Whenever a **new meeting is scheduled** or an **existing one is updated** in your calendar, this workflow performs the following actions:

### 🔍 Step 1: Extract Meeting Details

Triggered by changes in your **Google Calendar**, the workflow captures key metadata:

* Meeting **title**
* **Attendees**
* **Duration**
* Meeting **description**

### 🤖 Step 2: Evaluate Meeting Usefulness via AI

These details are passed to an **AI service** (e.g., OpenAI’s ChatGPT) which uses custom scoring logic to determine if the meeting is **worth attending** based on predefined usefulness metrics (e.g., purpose clarity, participant value, context redundancy).

### 📊 Step 3: Receive Usefulness Score

Once the usefulness score is returned, the system makes an informed decision:

---

## 🚦 Decision Logic

If the AI predicts a **low-value meeting**:

### 📨 1. Notify the User

A Slack message is sent to the attendee with:

* The **AI’s reasoning**
* A suggestion on whether to accept or decline

### 🗑️ 2. Cancel the Meeting (Conditional)

If the user responds confirming to decline:

* The meeting is automatically **deleted** from Google Calendar

### 💬 3. Notify the Organizer & Attendees

A Slack message is sent to:

* Politely **decline the meeting**
* Offer an **asynchronous alternative**, like sharing a document or written update

---

## ✅ Outcome

This workflow empowers users to:

* Regain control over their calendars
* Eliminate low-value, time-wasting meetings
* Encourage a culture of **async-first communication**

---

## 🔧 Tools & Services Used

| Tool                | Action                                                  |
| ------------------- | ------------------------------------------------------- |
| **Google Calendar** | Trigger on new/updated meeting, optionally delete event |
| **OpenAI ChatGPT**  | Score meeting usefulness                                |
| **Slack**           | Notify users, send DMs to organizers & attendees        |

---

## 🧩 Example Use Case

> "Rohit schedules a 1:1 meeting titled *Weekly Sync*. The AI finds that the purpose is unclear, the same agenda is repeated weekly, and there’s no new input needed. A Slack message is sent suggesting to skip and send a quick status update instead. Rohit agrees. The meeting is deleted and all involved receive a respectful async alternative message."

---

## 🚀 Future Improvements

* Customize usefulness metrics based on roles or teams
* Add options to reschedule instead of decline
* Log all AI decisions in Notion or Google Sheets for transparency

---
Here's a zap link to if you would like to test this out on your own: https://agents.zapier.com/copy/5c1d4a90-af11-42cc-9033-a19025ab3b22

