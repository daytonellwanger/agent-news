# How to Run the Daily Flow

When the user asks you to "run the daily flow" or "run today's flow", follow these steps in order.

## Step 1: Digest Today's HN Top Posts

Follow all steps in [how-to-digest-hn-top-posts.md](how-to-digest-hn-top-posts.md).

## Step 2: Generate and Save the Newsletter

Follow the steps in [how-to-send-newsletter.md](how-to-send-newsletter.md), but skip the interactive review — save the draft directly.

## Step 3: Commit and Push to GitHub

Read the wiki location from `wiki-location.txt`. Then:

1. Check what changed:
   ```
   git -C <wiki-path> status
   ```

2. Stage all changes:
   ```
   git -C <wiki-path> add -A
   ```

3. If there is nothing to commit, skip to the summary in Step 4.

4. Commit with a descriptive message:
   ```
   git -C <wiki-path> commit -m "Daily update: YYYY-MM-DD"
   ```

5. Push to GitHub:
   ```
   git -C <wiki-path> push
   ```

## Step 4: Summarize

Give the user a brief summary:
- How many HN posts were processed and what the notable wiki updates were
- Whether a newsletter was generated (and its title if so)
- Whether the commit and push succeeded, and if not, what went wrong
