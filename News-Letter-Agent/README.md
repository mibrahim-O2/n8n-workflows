📧 News-Letter-Agent — README

🧠 Overview

News-Letter-Agent is an automated newsletter generation workflow built
for n8n, integrating AI-powered tools like Google Gemini (PaLM) and
Tavily Search API to automatically curate, synthesize, and draft a
weekly business newsletter.

This automation is designed to run on a weekly schedule, gather the
latest AI-related business news, generate structured content using AI
agents, and create a formatted email draft in Gmail — ready for review
and distribution.

------------------------------------------------------------------------

⚙️ Workflow Summary

1. Schedule Trigger

-   Node: Schedule Trigger
-   Purpose: Runs the automation every week at 9 AM.
-   Type: n8n-nodes-base.scheduleTrigger
-   Output: Initiates the workflow on a timed interval.

------------------------------------------------------------------------

2. Search (Tavily News API)

-   Node: Search

-   Purpose: Searches for trending weekly articles related to “AI
    adoption for small businesses.”

-   Parameters:

    -   Topic: news
    -   Max Results: 3
    -   Time Range: week

-   Credentials: Tavily API

-   Output: 3 summarized news results for AI-related business trends.

------------------------------------------------------------------------

3. Planning Agent

-   Node: Planning-Agent

-   Purpose: Uses a large language model (via Gemini) to propose:

    -   A catchy newsletter title (≤ 80 chars)
    -   3 concise topic ideas (3–5 words each) relevant to
        small-business leaders

-   Prompt Role: “Expert newsletter planner”

-   Schema Constraints:

        {
          "title": "string",
          "topics": ["string", "string", "string"]
        }

------------------------------------------------------------------------

4. Structured Output Parser

-   Node: Structured Output Parser
-   Purpose: Ensures the AI output conforms to a strict schema (title +
    3 topics).

------------------------------------------------------------------------

5. Split Out

-   Node: Split Out
-   Purpose: Separates each topic (from the topics array) into
    individual items for further article generation.

------------------------------------------------------------------------

6. Topic Search (Tavily)

-   Node: Search1

-   Purpose: Conducts deeper searches for each proposed topic.

-   Parameters:

    -   Topic: general
    -   Time Range: month
    -   Include Raw Content: true

-   Output: 3 sets of detailed results (one per topic).

------------------------------------------------------------------------

7. Section Writer Agent

-   Node: Section-Writer-Agent

-   Purpose: Writes a 350–500 word Markdown section for each topic.

-   Prompt Role: “Professional newsletter section writer”

-   Output Requirements:

    -   Start with ## <topic>
    -   Cite facts using superscripts [1], [2]
    -   Add a “Sources” list at the end
    -   Tone: expert, engaging, factual

------------------------------------------------------------------------

8. Aggregate

-   Node: Aggregate
-   Purpose: Combines the 3 separate topic sections into one structured
    collection.

------------------------------------------------------------------------

9. Editor Agent

-   Node: Editor

-   Purpose: Acts as the newsletter editor that compiles all content
    into a cohesive HTML email layout.

-   Prompt Role: “Newsletter editor and layout stylist”

-   Output Schema:

        {
          "subject": "string",
          "content": "string (HTML)"
        }

-   Output Features:

    -   Header with title and date
    -   Short intro paragraph
    -   3 HTML-converted sections
    -   “Key Sources” list
    -   Sign-off note
    -   Accessibility-friendly, inline CSS
    -   No external JS/CSS

------------------------------------------------------------------------

10. Structured Output Parser (Final)

-   Node: Structured Output Parser1

-   Purpose: Validates the final newsletter structure before sending.

-   Fields:

    -   subject — Email subject line
    -   content — HTML email body

------------------------------------------------------------------------

11. Gmail Draft Creation

-   Node: Create a draft
-   Purpose: Creates an HTML email draft in Gmail with the generated
    newsletter.
-   Credentials: Gmail OAuth2
-   Output: Ready-to-review draft email in the connected Gmail account.

------------------------------------------------------------------------

🧩 Core Technologies

  ------------------------------------------------------------------------
  Component              Role                 Integration
  ---------------------- -------------------- ----------------------------
  n8n                    Workflow             Automates end-to-end flow
                         orchestration        

  Tavily API             Web & news search    Article discovery

  Google Gemini (PaLM)   LLM text generation  Planning, writing, and
                                              editing

  Gmail API              Email draft creation Publishes newsletter draft
  ------------------------------------------------------------------------

------------------------------------------------------------------------

🕐 Execution Flow (Simplified)

    Schedule Trigger
       ↓
    Tavily Search → Planning Agent → Structured Parser
       ↓
    Split Out (3 topics)
       ↓
    Tavily Search (per topic)
       ↓
    Section Writer Agent
       ↓
    Aggregate
       ↓
    Editor Agent → Structured Parser
       ↓
    Gmail Draft Creation

------------------------------------------------------------------------

🧾 Example Output

Subject: “AI Productivity Revolution for Small Businesses” Body (HTML):

-   Header: Title + Date
-   Intro paragraph
-   3 topic sections (e.g. AI Agents for Productivity, Google’s Unified
    AI Tools, Global AI Investment Trends)
-   Key Sources list
-   Friendly sign-off

------------------------------------------------------------------------

📅 Schedule & Automation

-   Runs: Weekly, every Monday at 9 AM
-   Frequency: Configurable in the Schedule Trigger node.
-   Purpose: Automates newsletter generation — no manual input required.

------------------------------------------------------------------------

🚀 Setup Instructions

1.  Import the JSON file into your n8n instance.

2.  Add credentials:

    -   Tavily API Key
    -   Google Gemini (PaLM) API credentials
    -   Gmail OAuth2 account

3.  Edit the search query (default: “AI adoption for small businesses”)
    if targeting other domains.

4.  Activate the workflow to run on schedule or manually trigger it.

------------------------------------------------------------------------

📚 Output Example Summary

  Field      Description
  ---------- -----------------------------------
  title      Catchy weekly newsletter title
  topics     3 key focus areas
  sections   AI-written Markdown sections
  subject    Email subject line
  content    HTML-formatted newsletter body
  draft      Created in Gmail for final review

------------------------------------------------------------------------

🧩 Use Cases

-   Automated AI newsletter creation
-   Weekly business intelligence digests
-   AI-driven editorial pipelines
-   Content marketing automation

------------------------------------------------------------------------

🧾 License

This workflow JSON is for educational and internal automation purposes.
Check third-party APIs (Tavily, Google, Gmail) for respective usage and
rate limits.

------------------------------------------------------------------------
