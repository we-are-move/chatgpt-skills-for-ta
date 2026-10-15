# ChatGPT Skills for TA

Created by Move · [wearemove.com](https://www.wearemove.com/)

Move's full TA Hiring Stack, packaged as **one plugin** in **one marketplace**. Version **0.2.0** contains **13 skills covering 24 hiring workflows**, including the LinkedIn Profile Auditor and the full **66-prompt TA Prompt Bank**.

## Install in the ChatGPT desktop app

1. Open **Plugins → Personal → Add plugin marketplace**.
2. Paste **https://github.com/we-are-move/chatgpt-skills-for-ta** into **Source**. Leave **Git ref** and **Sparse paths** blank.
3. Select **Add marketplace**, then go back to **Plugins → Personal**. **ChatGPT Skills for TA** will now be listed there. Open it, click **Install**, and wait for the installation to finish.
4. Once installation is complete, start a **new chat** and select a skill, or ask: **Show me the hiring skills and prompts available.**

Adding the marketplace makes the plugin available. Installing the plugin installs the complete collection; individual skills do not need separate installation. Availability can depend on app version and workspace policies.

## Update an existing pilot installation

Refresh or sync **ChatGPT Skills for TA** in your marketplace settings, then update the plugin if offered. Start a fresh chat after the update. If it still shows the one-skill pilot, remove and re-add the marketplace using the same repository link, then reinstall the plugin. Your pilot installation must refresh its cached copy to see the new skills.

## Included skills

| Skill | What it does | Requirements |
|---|---|---|
| [talent-market-mapper](plugins/chatgpt-skills-for-ta/skills/talent-market-mapper/SKILL.md) | Talent pool sizing, competitor research and sourcing pools | Web search; Node.js for Word reports |
| [job-spec-auditor](plugins/chatgpt-skills-for-ta/skills/job-spec-auditor/SKILL.md) | Job spec audit and rewrite | Document creation for Word output; copy-ready fallback |
| [role-calibrator](plugins/chatgpt-skills-for-ta/skills/role-calibrator/SKILL.md) | Role seniority, scope and title alignment | Chat inputs |
| [calibration-archetypes](plugins/chatgpt-skills-for-ta/skills/calibration-archetypes/SKILL.md) | Candidate archetypes and hiring-manager calibration | Web search; Node.js for Word output |
| [shortlist-builder](plugins/chatgpt-skills-for-ta/skills/shortlist-builder/SKILL.md) | Evidence-based candidate shortlists and screening gaps | Local file access; Node.js |
| [candidate-outreach-writer](plugins/chatgpt-skills-for-ta/skills/candidate-outreach-writer/SKILL.md) | Four-touch outreach campaign and LinkedIn DM | Tone-of-voice input; Node.js |
| [outreach-intelligence](plugins/chatgpt-skills-for-ta/skills/outreach-intelligence/SKILL.md) | Reply analysis, decline reasons and outreach tracker | Python: pandas/openpyxl; Node.js |
| [interview-pack-builder](plugins/chatgpt-skills-for-ta/skills/interview-pack-builder/SKILL.md) | Recruiter and hiring-manager packs, question banks and assessments | Intake, spec and evaluation philosophy; Node.js |
| [motivation-discovery](plugins/chatgpt-skills-for-ta/skills/motivation-discovery/SKILL.md) | Screening call guide and candidate motivation summary | Node.js for Word guide; chat for summaries |
| [hm-weekly-update](plugins/chatgpt-skills-for-ta/skills/hm-weekly-update/SKILL.md) | Hiring-manager updates for Slack, Teams or email | Chat; connected Slack and explicit approval to post |
| [pipeline-analyst](plugins/chatgpt-skills-for-ta/skills/pipeline-analyst/SKILL.md) | ATS triage, funnel analytics and pipeline workbook | Python: pandas/openpyxl; Node.js |
| [linkedin-profile-auditor](plugins/chatgpt-skills-for-ta/skills/linkedin-profile-auditor/SKILL.md) | Recruiter LinkedIn profile audit and rewrites | Profile text/PDF and screenshots for visual sections |
| [ta-prompt-bank](plugins/chatgpt-skills-for-ta/skills/ta-prompt-bank/SKILL.md) | 66 prompts across the hiring lifecycle and AI adoption | Depends on the chosen prompt |

Several of the 24 workflows use the same skill. For example, intake codification, screening structure, question banks and AI/skills testing are handled by Interview Pack Builder. Intake prep, role personas, persona interviews, message crafting, interviewer briefings/coaching, rejection and candidate advocacy also have dedicated numbered prompts in TA Prompt Bank. Slack integration is an optional delivery mode of Hiring Manager Weekly Update.

## Runtime requirements

Chat-based workflows can work without local code execution. Word and spreadsheet workflows need a session with shell/file access, such as a suitable ChatGPT Work or Codex desktop session. Installing this plugin does not automatically install Node.js or Python packages or connect external services.

- **Word builders:** Node.js and `docx` 9.6.1. Prefer a host-provided package; otherwise install it in the task working folder with `npm install --no-audit --no-fund docx@9.6.1`.
- **Spreadsheet analysis:** Python, `pandas` and `openpyxl`.
- **Research:** available web search and source-page access for market mapping and archetypes.
- **Slack:** the user's connected Slack account, a specified destination and explicit approval before posting. Without Slack, the update is provided as copy-ready text.

The campaign and hiring-pack skills include reusable company-input templates. Complete these, or use the skills' guided questions, before generating documents. Move branding, methodology and discovery-call links are preserved.

## Codex CLI alternative

```sh
codex plugin marketplace add https://github.com/we-are-move/chatgpt-skills-for-ta
codex plugin add chatgpt-skills-for-ta@chatgpt-skills-for-ta-marketplace
```

For an existing Git-backed source, run `codex plugin marketplace upgrade chatgpt-skills-for-ta-marketplace`, then refresh the installed plugin and start a new session.

## Validation status

The one-skill marketplace installation and Role Calibrator pilot were successfully tested before this expansion. The expanded package is checked for valid skill metadata, complete bundled resources, cross-skill references, JavaScript syntax and Word-builder execution on synthetic configurations. These package/runtime checks do not establish the quality of every hiring workflow or visual layout of every generated document.

## About and rights

Created by [Move](https://www.wearemove.com/). This is an independently created plugin, not an official OpenAI product. Move retains rights to its original methodology and content; no open-source licence is granted by this package.

[Plugin packaging guidance](https://developers.openai.com/plugins/build/plugins)
