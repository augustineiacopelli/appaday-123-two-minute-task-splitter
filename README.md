# App 123: Two-Minute Rule Task Splitter

Part of [AppADay](https://augustineiacopelli.github.io/appaday/), a project to design, build, and publish one complete web app every day.

## What it does

Applies David Allen's two-minute rule to whatever task you're avoiding. Describe the task, and Claude breaks it into an ordered checklist of small, concrete subtasks with a time estimate for each one. Check items off as you go and watch a live progress bar fill in. If the breakdown isn't quite right, add a refinement instruction and regenerate it.

## Category

AI-Powered Tools (A)

## How it works

A single self-contained `index.html` file. No build step, no framework, no dependencies beyond an optional Google Fonts link.

The Claude API key and a session name live in the settings modal (gear icon) and are stored only in the browser's `localStorage`, never on the main screen. Requests go straight from the browser to the Anthropic API using the `anthropic-dangerous-direct-browser-access` header, with the key read fresh from storage on every call. The current task, any refinement instructions, and the full subtask checklist (including completion state) are also saved to `localStorage`, so a breakdown in progress survives a page reload.

Model used: `claude-sonnet-5`.

## Try it

[Live app](https://augustineiacopelli.github.io/appaday-123-two-minute-task-splitter/)
