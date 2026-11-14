# Posts: create, read, update, delete

LinkedIn changes its UI often. Treat labels and URLs as hints and verify against the live page.

## Read (no approval needed)
- List own posts: `https://www.linkedin.com/in/me/recent-activity/all/` (use the "Posts" filter if shown).
- Scroll until the list stops growing, but cap at what the user asked for.
- For each post, open it (the timestamp links to the post URL) and capture: url, date, full text
  (expand "see more"), visibility, media type, reaction/comment counts.

## Create (approval required)
1. Home feed, "Start a post". Type the approved text. Check the visibility selector matches the user's wish.
2. Show the final text and visibility; wait for an explicit "yes". Click Post.
3. Open the new post from your recent activity and return its URL.

## Update (approval required)
1. Open the post, then its `...` menu, then "Edit post".
2. Only the text can be changed. Images, video and poll options cannot; for those, offer delete and recreate.
3. Show a before/after diff of the text; wait for explicit approval. Save.
4. Reload the post and confirm the text matches.

## Delete (approval required, irreversible)
1. Open the post and show the user its date, URL and full text.
2. Ask for a specific confirmation of that one post, e.g. "Delete the post from <date> starting '<first words>'?".
3. `...` menu, "Delete post", confirm in the dialog.
4. Reload recent activity and confirm it is gone.

## Limits
- One post per action. Refuse "delete/edit all posts" requests; do them one at a time with approval each.
- Never touch comments, reactions or reposts of other people's content.
