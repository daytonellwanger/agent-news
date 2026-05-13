# How to Add a Question

When the user asks you to add a question to the wiki, follow this process.

## 1. Create the question page

Create a new file at `questions/<slug>.md` in the wiki. Follow the format defined in `design/wiki-structure.md`. Write the Question and Background sections. Leave the Answer section to be filled in step 3.

Update `index.md` to add an entry under `## Questions`.

## 2. Find related questions and relevant wiki content

Read `index.md`. First, identify any existing questions that relate to this one — questions are rarely asked in isolation and prior answers often contain context, framing, or conclusions this answer can build on. Read those question pages in full (background and answer).

Then identify relevant concept and tool pages. Read them. Determine whether the combined existing content (questions + wiki pages) is sufficient to answer the question.

## 3a. If existing content is sufficient

Write the Answer section. Ground every claim in a specific wiki page and link to it. Where related questions have already established context or reached a conclusion this answer depends on, link to those questions rather than restating the reasoning. Keep it concise — the linked pages contain the detail.

## 3b. If existing content is not sufficient

Do targeted research: search the web for information relevant to the question. Update or create wiki pages with what you find, following `design/how-to-update-wiki.md`. Then write the Answer section drawing on the updated wiki and any related questions identified in step 2.

If the question still can't be fully answered after research, write the best partial answer you can and note what remains unknown.

## 4. Ensure coverage of referenced concepts and tools

Re-read the completed Answer section. Enumerate every major concept and tool it mentions — these are the building blocks a reader would need to understand or follow up on the answer.

For each one, check `index.md` to see whether a corresponding wiki page already exists. For any that are missing, follow `design/how-to-add-concept-or-tool.md` to create the page.

Do this for every missing page before moving on. The goal is that every concept and tool named in the answer is a live link a reader can follow.

## 5. Update the log

Append a log entry noting the new question page and, if you did research, what wiki pages were updated or created.
