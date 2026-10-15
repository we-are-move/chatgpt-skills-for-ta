# ChatGPT Skills for TA

A recruiting skills plugin by Move. This pilot contains **Role Calibrator** (`role-calibrator`), which assesses role seniority from a job spec or intake notes. It compares title and scope, identifies mismatches, and suggests hiring-manager and interview questions.

## Install in the ChatGPT desktop app

1. Open **Plugins**, choose **Personal**, then **Add plugin marketplace**.
2. In **Source**, paste `https://github.com/we-are-move/chatgpt-skills-for-ta`. Leave **Git ref** and **Sparse paths** blank.
3. Select **Add marketplace**, open **ChatGPT Skills for TA** and install the plugin once.
4. Start a new chat. Select the installed Role Calibrator skill, or ask: **Use role-calibrator to assess this role**, followed by a job spec.

Adding the marketplace makes its plugin available; installing the plugin adds every skill bundled in it. Version 0.1.0 has one skill. The same repository can later distribute the full collection.

## Alternative: Codex CLI

Replace `https://github.com/we-are-move/chatgpt-skills-for-ta` with this repository's GitHub URL:

```sh
codex plugin marketplace add https://github.com/we-are-move/chatgpt-skills-for-ta
codex plugin add chatgpt-skills-for-ta@chatgpt-skills-for-ta-marketplace
```

Start a fresh session after installation.

## What to provide

Paste a job spec or intake notes. Company stage, pay band and an internal level ladder are optional. The skill works in chat and needs no Node.js, Python, web search or external service connection.

## Pilot test

Use a tester who does not already have `role-calibrator` installed as a standalone skill. Record whether the marketplace adds successfully, the plugin installs, and the skill appears in a fresh chat. Run a real job spec and check that the assessment quotes responsibilities, distinguishes individual-contributor and management scope, and does not invent salary benchmarks. If it fails, record the app version and exact error.

The standalone skill has been successfully tested in Codex. Installation from GitHub and execution in another person's ChatGPT remain to be tested. Account and workspace permissions may affect availability.

## About

Created by Move: https://www.wearemove.com

This is an independently created plugin, not an official OpenAI product. Move retains rights to its original methodology and content; no open-source licence is granted by this pilot.

Plugin packaging documentation: https://developers.openai.com/plugins/build/plugins
