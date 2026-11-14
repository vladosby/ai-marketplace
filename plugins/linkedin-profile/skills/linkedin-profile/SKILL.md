---
name: linkedin-profile
description: Read the user's full LinkedIn profile, edit profile sections (About, experience, education, skills, certifications, projects, languages) and write posts, by driving a logged-in browser. Use when the user asks to view, export, update or improve their own LinkedIn profile or to draft and publish a LinkedIn post.
---

# LinkedIn profile via browser

Works with any agent that has a browser tool able to: open a URL, read the page
(accessibility snapshot or text), click, type, and take a screenshot. Examples: Playwright MCP,
Chrome DevTools MCP, a built-in browser. Only the user's **own** account is in scope.

Automating LinkedIn is against its terms of service. Keep volume low, act only on request, and
follow `references/safety.md`.

## Workflow

1. **Session check.** Open `https://www.linkedin.com/in/me/`. If a login or checkpoint page appears,
   stop and ask the user to sign in in the browser window, then continue. Never ask for or type
   credentials, 2FA codes or cookies.
2. **Read the full profile.** Follow `references/sections.md` to visit the profile and each section's
   "show all" page. Return data in the shape of `references/profile-schema.md`. Reading needs no approval.
3. **Edit a section.** Open the section's edit form, read the current values, then show the user a
   before/after diff and **wait for explicit approval**. Save, then re-read the section and confirm
   the saved values match.
4. **Post.** Draft the text, show it, **wait for explicit approval**, publish, then return the post URL.
5. **Report.** Say exactly what changed, or that nothing did.

## Rules

- One write action at a time. No bulk edits, no loops over many sections without approval each time.
- Do not touch messaging, connections, invitations, settings, or other people's content.
- If the page differs from what the reference files describe, trust what you see and tell the user.
- Stop and report on CAPTCHA, checkpoint, "unusual activity" notices or unexpected dialogs.
