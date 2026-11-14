# OSS Writing Style Guide

This guide covers the words in and around a software product: interface text, documentation, release notes, help articles, and the post that announces a new feature. It's for anyone who writes those words, whether that's a technical writer, a designer, an engineer, or a product manager.

## How to use this guide

- Read [Voice](#voice) and [The short version](#the-short-version) once. Together they cover most edits.
- Look up everything else when a question comes up. Each section stands on its own.
- Examples show a rule as a before and an after. They illustrate the rule. They aren't phrases to find and replace.
- Examples use a fictional project-and-task app with projects, tasks, team members, a reporting console, and a sync connector. Product names in examples are made up.
- A **Limit** under a rule marks the point where applying the rule would change a fact. Stop there and ask the author.
- The guide uses US English spelling and conventions. If your team writes another variety of English, say so in your fork and keep the rest.
- Some rules are house choices rather than grammar: sentence case, no em dashes, no semicolons, _select_ rather than _click._ If your team decides differently, change the rule in your fork and apply the change consistently. The reasoning beside each rule is there so you can make that call.
- Apply the guide to new text and to text you're already changing. Don't open a document only to restyle it.
- Two tables under [Terminology](#terminology) are templates: your product names and the third-party brands you write about. Fill them in before you apply the guide.

## Contents

1. [Voice](#voice)
2. [The short version](#the-short-version)
3. [Editing someone else's text](#editing-someone-elses-text)
4. [Sentences](#sentences)
5. [Talking to the reader](#talking-to-the-reader)
6. [Grammar checks](#grammar-checks)
7. [Capitalization](#capitalization)
8. [Terminology](#terminology)
9. [Writing about product behavior](#writing-about-product-behavior)
10. [UI text](#ui-text)
11. [Documentation](#documentation)
12. [Numbers](#numbers)
13. [Punctuation](#punctuation)
14. [Inclusive language](#inclusive-language)
15. [Writing for a global audience](#writing-for-a-global-audience)
16. [Text that sounds machine-written](#text-that-sounds-machine-written)
17. [Reviewing a draft](#reviewing-a-draft)

## Voice

Voice is the personality that stays the same everywhere the product speaks. Tone is how that voice adjusts to the moment. A product talking to someone who just lost an hour of work shouldn't sound the way it does on a welcome screen, but it should still sound like the same product.

### Four qualities

**Clear.** The reader understands it the first time. Use the common word, the short sentence, and the concrete example. If you had to read a sentence twice, rewrite it.

**Direct.** Lead with what the reader needs. Say what happened, what it means, and what to do next, in that order. Skip the warm-up.

**Warm.** Sound like a capable colleague, not a legal notice and not a cheerleader. Use contractions and everyday words. Be kind when something goes wrong, and don't gush when something goes right.

**Honest.** Describe what the product does today, not what it might do someday. Don't overpromise, don't hide limits, and don't let a feature sound smarter than it is.

### Adjust the tone to the moment

| Situation | What the reader feels | Tone | Example |
| --- | --- | --- | --- |
| **First use** | Curious, a little unsure | Encouraging, brief | Create your first project to start tracking work. |
| **Routine task** | Focused | Neutral, out of the way | Project saved. |
| **An error the reader can fix** | Interrupted | Calm, specific | The file is larger than 25 MB. Choose a smaller file. |
| **Data loss or an outage** | Worried | Serious and plain | Changes from the last 10 minutes weren't saved. Check the activity log to see which ones. |
| **Security or legal** | Cautious | Precise | Anyone with this link can view the project. |
| **A milestone** | Pleased | Light, still short | You closed 100 tasks this month. |

Humor is optional and rarely worth the risk. It doesn't translate well, it wears thin on the fifth viewing, and it lands badly on someone having a bad day. Never joke in an error message.

## The short version

Twelve rules cover most edits. Each one links to its full section.

| Rule | Before | After |
| --- | --- | --- |
| **1. [Lead with the point](#lead-with-the-point)** | To make sure your team always sees the latest numbers, the dashboard refreshes every 5 minutes. | The dashboard refreshes every 5 minutes, so your team sees the latest numbers. |
| **2. [Write to _you_](#write-to-you)** | The user receives an email when a task is assigned. | You get an email when someone assigns you a task. |
| **3. [Cut words, not facts](#cut-words-not-facts)** | The system provides the ability to filter tasks by due date. | Filter tasks by due date. |
| **4. [Use sentence case](#sentence-case-by-default)** | Create A New Project | Create a new project |
| **5. [Prefer active voice](#use-active-voice)** | The report is generated by the scheduler every Monday. | The scheduler generates the report every Monday. |
| **6. [Use present tense](#use-present-tense)** | When you select **Save**, the dialog will close. | When you select **Save**, the dialog closes. |
| **7. [Use the serial comma](#commas)** | Projects, tasks and comments | Projects, tasks, and comments |
| **8. [Skip em dashes and semicolons](#dashes)** | Archived projects — those older than a year — are read-only. | Archived projects, those older than a year, are read-only. |
| **9. [Name UI labels exactly](#ui-labels-in-documentation)** | Click the save changes button. | Select **Save changes**. |
| **10. [Say what went wrong and what to do](#error-messages)** | Upload failed. | The file is larger than 25 MB. Choose a smaller file. |
| **11. [Describe only what ships](#describe-only-what-ships-today)** | Two-way calendar sync is coming soon. | (Move it to the release notes or the roadmap.) |
| **12. [Products don't think](#products-arent-people)** | The assistant understands what you mean. | The assistant matches your question to related help articles. |

Rules 1 through 10 are edits anyone can make. Rules 11 and 12 need the author, because they're about facts.

## Editing someone else's text

When you edit text that someone has already checked for accuracy, your job is presentation. The author knows things you don't: what shipped, what's configurable, what the real limit is. A style edit that changes a fact is a bug, even when the new sentence reads better.

**You can change** punctuation, capitalization, spelling, word order, sentence breaks, list and table structure, how UI labels are formatted, terminology (to the canonical forms in [Terminology](#terminology)), and word choice where the meaning stays identical.

**Don't change** any fact, number, date, version, name, step, sequence, condition, scope, or claim. Don't add information the source doesn't contain. Don't delete a statement because it looks wrong or out of date. Ask instead.

**Don't touch** code and code blocks, commands, file paths, URLs, quoted error text, identifiers, version strings, string-table keys, placeholder tokens, or legal text.

**If the text already follows the rules, leave it.** Rewriting correct text to suit your taste creates review work and risk without improving anything.

### Edit or flag

Some problems you can fix yourself. Others need the author. When a fix would need a fact you don't have, leave the text as it is and write the author a note that says where, what's missing, and which rule applies.

| Problem | What to do |
| --- | --- |
| An em dash, title case, or a missing serial comma | Edit |
| _The user_ where the reader is meant | Edit |
| "Updates in near real time," with no interval anywhere in the source | Flag: state the interval |
| A feature described in the future tense | Flag: is this released? |
| An error message with no next step | Flag: what should the reader do? |
| An acronym with no expansion anywhere in the source | Flag: expand it |
| Something that looks like a real key, password, or customer record in a sample | Flag: replace it with a placeholder |
| A sentence that might be wrong | Flag. Don't fix facts. |

### When rules conflict

1. A fact in the source is never changed to satisfy a rule.
2. An existing UI label is copied exactly, even if it breaks a rule.
3. Where this guide is silent, ask. Don't guess.

## Sentences

These rules apply to a button label as much as to a deployment guide.

### Cut words, not facts

Every word should do work. Long phrases that mean the same as a short one are the easiest cut.

| Cut this | Write this |
| --- | --- |
| in order to | to |
| has the ability to, is able to | can |
| provides the capability to | lets you |
| used for the purpose of | used for |
| owing to the fact that, due to the fact that | because |
| in spite of the fact that | although |
| in the event that | if |
| prior to | before |
| at this point in time | now |
| the question as to whether | whether |
| in a timely manner | promptly |
| a number of | several, or the number |

| Before | After |
| --- | --- |
| The system provides the capability to assign tasks to teammates who are currently available. | Assign tasks to available teammates. |
| Click here to save your changes | Save |

**Limit.** A qualifier that describes real behavior is a fact, not filler. _May, up to, at least, typically,_ and _only when_ tell the reader how the product behaves. Keep them.

### Say what is, not what isn't

A positive statement is usually shorter and easier to follow. Use it when it means exactly the same thing.

| Before | After |
| --- | --- |
| The report does not include test accounts. | The report excludes test accounts. |
| Notifications are not turned on. | Notifications are off. |

**Limit.** Don't convert a prohibition ("Do not restart the service during a deployment") or a scope exclusion ("This setting does not apply to archived projects"). The negative is the fact. Don't infer a positive the source didn't state: "isn't signed out for 8 hours" doesn't mean "stays signed in for 8 hours."

### Flag vague claims, don't sharpen them

A vague phrase usually hides a missing fact: an interval, a count, a limit, or a condition. If you're editing, you can't supply it.

| Vague phrase | What's missing |
| --- | --- |
| Updates in near real time. | The refresh interval |
| Shows key events. | Which events, and how many? |
| Scales to meet enterprise needs. | The limit, or cut the sentence |

Rewrite only when the specific value appears elsewhere in the source. Then use it.

### Use nouns and verbs

Nouns and verbs carry a sentence. Most adjectives and adverbs are padding.

| Before | After |
| --- | --- |
| The backlog was very quickly cleared out. | The backlog cleared. |
| Significantly reduces overall build time. | Reduces build time. |

The words to cut are in the [word list](#word-list).

### Keep parallel ideas parallel

Items in a list, headings at one level, and steps in a procedure take the same grammatical form.

| Before | After |
| --- | --- |
| Create a project, members should be added, and then the access rule needs setting. | Create a project. Add members. Set the access rule. |
| Pending, Being processed, Done | Pending, Processing, Done |

### Keep modifiers next to what they modify

A modifier attaches to the nearest thing it could describe. Put it next to the word you mean.

| Before | After |
| --- | --- |
| Archived projects are only exported on request. | Archived projects are exported only on request. |
| After failing three health checks, the system marks the server as Offline. | A server that fails three health checks is marked Offline. |
| After saving the file, the dialog closes. | After you save the file, the dialog closes. |

In the second and third befores, the opening phrase attaches to the wrong subject. The system didn't fail the health checks, and the dialog didn't save anything.

### Lead with the point

Readers scan. Put the key word first in a heading, a label, a list item, and the first sentence of a paragraph. Inside a sentence, don't let the point trail off into a weak closing clause.

| Before | After |
| --- | --- |
| An error occurred when the system attempted to export, which may be related to the file path. | Export failed. Check the file path. |
| Settings for the project | Project settings |

### Use present tense

_Opens,_ not _will open._ Present tense describes how the product behaves every time.

**Limit.** A sentence about the future ("will be available in the next release") is a fact about timing. Don't move it to the present. See [Describe only what ships today](#describe-only-what-ships-today).

### Use active voice

In active voice, the subject does the action: "The connector retries the request." It's shorter and it tells the reader who acts.

**Limit.** Convert passive to active only when the actor is named or obvious. "The file is deleted" has no actor. Leave it, or flag it. Passive is also right when it keeps blame off the reader ("The password wasn't recognized") or when the receiver is the point ("Requests are sent to the first available server").

### Write facts as statements and steps as commands

State facts plainly: "The dashboard refreshes every 15 seconds." Give instructions as commands: "Select **Save**." Don't phrase advice as a wish. Write "Back up the database before you upgrade," not "It is recommended that you consider backing up the database."

### Use contractions

Common contractions such as _it's, you're, don't, can't,_ and _isn't_ make text sound like a person wrote it. Avoid unusual ones (_it'd, should've, there're_) and contractions of nouns ("the project's been archived").

**Limit.** Legal text keeps its exact wording.

### Choose plain words

Prefer the short, common word: _use_ over _utilize,_ _help_ over _facilitate,_ _through_ over _via._ The [word list](#word-list) has the full set.

### Watch words ending in _-ing_

A word ending in _-ing_ can be a verb, a noun, or an adjective, so a short phrase can mean two things. The heading "Scheduling reports" could mean "how to schedule a report" or "reports about scheduling." Pick the version you mean: "Schedule a report."

### Keep chains of prepositions short

More than two prepositional phrases in a row are hard to follow.

| Before | After |
| --- | --- |
| the status of the sync of the files in the folder of the project | the sync status for files in the project folder |

### Paragraphs

These apply to documentation.

**One topic per paragraph, stated in the first sentence.** Someone who reads only the first sentence of each paragraph should still follow the argument. Reorder sentences to get there. Don't cut one that carries a fact.

**Don't explain twice.** If the same fact appears twice in different words, keep the clearer copy and delete the other. If the two copies differ in substance, flag the conflict.

## Talking to the reader

### Write to you

Most product content has one reader: the person who uses the product day to day to get their work done. Someone who opens the product, reads what it shows, and changes settings as part of the job.

Address that person as _you._ Don't write _the user._ The rule is the same for UI and documentation. In the UI, the reader is the one acting. In documentation, _you_ keeps the writing direct and keeps the reader's job in view. Cut _you can_ when the sentence works without it.

| Before | After |
| --- | --- |
| The user can assign a task to any available teammate. | You can assign a task to any available teammate. |
| After the user saves the change, users see the new project on their next login. | After you save the change, team members see the new project the next time they sign in. |
| You can export the report as a CSV file. | Export the report as a CSV file. |

**Exception.** _User_ is the right word for a category, as in _user permissions_ or _user account,_ and in developer documentation, where it means the end user of the software your reader is building.

### Name everyone else by role

Everyone else in the story gets a role name, not a pronoun: _the admin, the customer, the reviewer, the team lead._

### Use _we_ only when the company is speaking

_We_ puts the company at the center. Use it only when the company has to be the speaker, such as in a privacy notice, a statement about how data is handled, or an update about an outage.

> We encrypt your files at rest and in transit.
>
> We're investigating the outage and will post an update here within 30 minutes.

Don't use _we_ to give advice. "We recommend that you back up your data" becomes "Back up your data."

### _I, me,_ and _my_

**In UI**, first person is fine when the reader is the one speaking, such as in a checkbox or a toggle: "Keep me signed in," "Email me when someone mentions me." Use _My_ in navigation only when it separates the reader's own content from shared content: **My tasks** next to **All tasks.** Don't mix _my_ and _your_ on the same screen.

**In documentation**, never use first person singular.

If a product has a named persona that speaks for itself, _I_ is fine in that persona's messages. Keep it consistent.

### Text the product generated

When the product did something on its own, use past tense so the reader knows it already happened, and make clear that a judgment was applied and may need review.

> A summary was drafted from the last 20 comments. Review it before you share it.

## Grammar checks

Most grammar takes care of itself in short, active sentences. These are the points that still trip people up.

### Agreement

- **Collective nouns** such as _team, company,_ and _organization_ take a singular verb and pronoun: "The team has its own workspace." If the point is the individuals, rewrite with a plural noun: "Team members have their own workspaces."
- **_And_ joins subjects into a plural:** "The owner and the admins approve changes."
- **_Or_ follows the nearest subject:** "The owner or the admins approve changes." "The admins or the owner approves changes."
- **_A number of_ is plural, _the number of_ is singular:** "A number of tasks are overdue." "The number of overdue tasks is shown in red."

### Pronouns

Use singular _they_ for a person whose gender isn't known or doesn't matter. For more, see [Inclusive language](#inclusive-language).

### Plurals and possessives

- Add a lowercase _s_ to make an acronym plural, with no apostrophe: _APIs, URLs._
- Decades take no apostrophe: _the 2020s._
- Don't write _(s)_ to mean one or more. "Select the file(s)" becomes "Select one or more files."
- Don't make a product name possessive. "Acme Assistant's answers" becomes "answers from Acme Assistant."
- _Its_ is possessive. _It's_ means _it is_ or _it has._

## Capitalization

### Sentence case by default

Use sentence case for headings, titles, labels, buttons, menu items, tooltips, column headers, and list items. Capitalize the first word and proper nouns. Everything else is lowercase.

> Invite people to a project
>
> Sync settings
>
> Release notes for version 4.2

In a heading or title, also capitalize the first word after a colon.

> Version 4.2: What changed for admins

### Proper nouns and common nouns

Capitalize the names of products, companies, people, places, events, and trademarks. Most technology terms are common nouns, so they're lowercase: _cloud computing, machine learning, open source, single sign-on, dashboard, workspace._ A feature is a common noun unless it has a branded name.

If you can't tell whether a word is a name, check the product's term list or a current dictionary. If it's still unclear, default to lowercase. When you're editing someone else's text, leave the case as it is and flag it.

### Other capitalization rules

- **Labels in documentation.** When you name an existing UI label, copy its capitalization from the source, even if it doesn't follow sentence case.
- **Generic UI elements** are lowercase in running text: _toolbar, menu, tab, dialog._
- **No all caps for emphasis.** In UI, a short badge (PREVIEW, BETA, NEW) is the one exception.
- **No internal capitals** unless the brand uses them. _GitHub_ keeps its capital H. A generic _report builder_ isn't _ReportBuilder._
- **Spelled-out acronyms** are lowercase unless they're proper nouns: _single sign-on (SSO)._
- **Slashes.** In a label, if the word before the slash is capitalized, capitalize the word after it: _On/Off._
- **Defined terms** keep the capitalization their definition gave them. See [Defined terms](#defined-terms).
- **Lowercase identifiers.** Don't start a sentence with a command or identifier that must stay lowercase. Rewrite: "The `npm` command installs the package."

### When title case is required

Use title case only for titles of published works, names of events, job titles directly before a person's name, and product names that are styled that way. When you need it:

- Capitalize the first and last words.
- Capitalize nouns, verbs (including _is_ and _be_), adjectives, adverbs, and pronouns.
- Lowercase _a, an,_ and _the_, the conjunctions _and, but, or, nor, for, so,_ and _yet,_ and prepositions of four or fewer letters, unless one of them is the first or last word.
- After a hyphen, capitalize the word if it would be capitalized on its own.

> A Field Guide to Release Notes
>
> What Is a Service Level Objective?
>
> Getting Started with Self-Hosted Runners

## Terminology

Consistent names make a document read as one product. Pick the canonical term once, then use it everywhere.

### Canonical product names

Use the full, approved product name on first mention in a section. Don't invent shorthand, and don't let a working title from a design doc reach a customer.

Keep a table of your product names and the aliases to retire. The row below is a fictional example of the format.

| Use this | Not this |
| --- | --- |
| **Acme Assistant** | Acme Assist, AcmeBot, the assistant bot |

After the first mention in a section, a short form such as _the Assistant_ is fine when the context is clear.

### Generic terms for capabilities

When you mean the category rather than the product, use a generic term, and use the same one every time. For an AI chat feature, pick _AI assistant_ or _virtual assistant_ and don't alternate among _assistant, bot, chatbot,_ and _agent_ in one document. _Agent_ is the riskiest of these, because it can also mean a person.

> Acme Assistant answers questions about project status. (the product)
>
> An AI assistant can handle routine questions without a person stepping in. (the capability)

If a word could mean either the product or the category, rewrite so it's clear. When you're editing someone else's text and can't tell which they meant, flag it.

### Defined terms

If a document defines a term, in a glossary or a definitions section, capitalize it the same way every time afterward. If the document doesn't define it, keep it lowercase. Don't capitalize a word because it looks important.

> A Maintenance Window is a scheduled period when updates can run. Create a Maintenance Window for each region.
>
> The backlog holds tasks that nobody has picked up yet. (not a defined term, so lowercase)

### Product terms must name real things

Before you use a product term, make sure it names something the reader can see or act on, such as a label, a menu, or a setting. A term that exists only in a design document sends readers looking for a screen that isn't there.

### Third-party brands and trademarks

Third-party products appear in integration and deployment content. Use the owner's exact casing everywhere.

Keep a table of the brands your content names. Set the symbol only after you check the owner's trademark guidelines, and record when you checked. The rows below show the format, and none of them has been checked.

| Write it as | Owner | Symbol at first mention | Checked |
| --- | --- | --- | --- |
| **GitHub** | GitHub, Inc. | Confirm | Not yet |
| **Salesforce** | Salesforce, Inc. | Confirm | Not yet |
| **Slack** | Slack Technologies, LLC | Confirm | Not yet |
| **Jira** | Atlassian Pty Ltd | Confirm | Not yet |

**In documentation,** put the symbol on the first mention in the body of the document, not in a heading. After that, use the plain name. End any document that names a third-party brand with an attribution line: "All product and company names are trademarks or registered trademarks of their respective owners." Have your legal team review it.

> The connector supports ExampleCloud® and SampleChat® workspaces. ExampleCloud projects are imported automatically. (fictional brands)

**In UI,** whether a symbol appears depends on the surface. See [Third-party brands in UI](#third-party-brands-in-ui).

More rules:

- If the source already shows a symbol, keep it. If the table says Confirm, add no symbol. Never switch ™ to ® or back on your own.
- If an owner restyles a brand, use the current form.
- Don't use a brand as a verb or a common noun. "Slack me" becomes "Send me a message in Slack."
- Don't add a symbol to a term that isn't a brand. For your own product names, follow your legal team's guidance.

### Acronyms and abbreviations

- **Spell out your own product and feature names.** Don't turn them into acronyms.
- **Spell out on first use.** Write the term, then the acronym in parentheses. After that, use the acronym alone within the same document or screen.
- **Skip the expansion for acronyms every reader knows,** such as USB, FAQ, URL, and PDF.
- **Skip the acronym for a term you use once.** Just spell it out.
- **Don't introduce an acronym in a heading.** Introduce it in the text that follows.
- **Lowercase the spelled-out form** unless it's a proper noun: _single sign-on (SSO), role-based access control (RBAC)._
- **Choose _a_ or _an_ by sound:** _an API, an SSO setting, a URL, an HTML file._
- **Don't make an acronym possessive.** "The API's limits" becomes "the API limits" or "the limits of the API."
- **Avoid Latin abbreviations.** Write _for example, that is,_ and _and so on._ Readers and translation tools misread _e.g., i.e.,_ and _etc._

When you're editing someone else's text, expand an acronym only if the expansion appears somewhere in the source. Otherwise, flag it.

### Word list

Words to use, words to avoid, and why. The Why column tells you when a rule doesn't apply. Add rows from your own reviews.

| Write | Instead of | Why |
| --- | --- | --- |
| **one generic term**, such as _AI assistant_ | alternating assistant, bot, chatbot, agent | Consistency. _Agent_ can also mean a person. |
| **you** | the user | One reader, addressed directly. _User_ stays as a category word. |
| **sign in** (verb), **sign-in** (noun) | log in, login | House style |
| **set up** (verb), **setup** (noun) | setup (as a verb) | The verb is two words |
| **email** | e-mail | Current spelling |
| **dialog** | dialog box, pop-up | Shortest clear term |
| **checkbox** | check box | Current spelling |
| **select** | click, tap | Works for every input method. Keys are still _pressed._ |
| **cyberattack**, **cyberthreat** | cyber attack, cyber-attack | One word |
| **use** | utilize, leverage | Plain word |
| **help** | facilitate, empower | Plain word. _Enable_ stays when it means turn on. |
| **through**, **by**, **using** | via | Plain word |
| **for example** | e.g. | Latin abbreviations confuse readers and translation tools |
| **that is** | i.e. | Same reason |
| **such as**, or name the items | etc. | Say what's included |
| (flag, don't rewrite) | always, never, guarantees, ensures, eliminates, perfect, applied to an outcome or to model behavior | A claim, not a style choice. Suggest _selects, ranks, estimates, predicts, recommends,_ or a plain statement of what the product does. |
| (flag, don't rewrite) | understands, knows, believes, thinks, applied to a product | Products don't have minds. Suggest _ranks, selects, estimates._ |
| (delete) | very, really, quite, rather, actually, basically, simply, just, easily, truly, genuinely, literally | Filler intensifiers |
| (delete) | seamlessly, robust, powerful, intuitive, cutting-edge, best-in-class, world-class | Marketing words that carry no fact |
| (keep, or flag) | may, might, could, typically, usually, up to, at least | A hedge that states real behavior is a fact. Cut it only when it's clearly filler. |

**Limit.** Delete a word from the delete rows only when it's working as an intensifier. _Just_ meaning "only" or "a moment ago," and _simply_ or _really_ inside a quotation or a product name, stay. In UI strings, a swap that would rename a label the product already uses everywhere, such as _Log in_ to _Sign in,_ is a product decision. Flag it rather than changing one screen.

## Writing about product behavior

Documentation makes promises. A sentence about a feature that hasn't shipped becomes a commitment someone has to keep, and a sentence about internal mechanics becomes a contract you can't change later. These rules keep documentation accurate without making it vague.

When you're editing someone else's text, these rules produce flags, not edits. You can't verify what has shipped, what's internal, or what's true. The author can.

### Describe only what ships today

Write about behavior that exists in the released product. Don't describe planned features, roadmap items, or capabilities behind a setting the reader can't turn on.

| Use this | Not this |
| --- | --- |
| **The dashboard reports response time by project.** | The dashboard will soon report response time by team member. |
| **Export runs on a daily schedule.** | Real-time export is coming in a future release. |

If readers need to know that something is planned, say so in release notes or a roadmap, not in a feature guide.

### Leave out internal implementation details

Describe what the product does and what the reader controls. Leave out service names, table names, polling intervals, cache behavior, and the order of internal calls. Those details change often, and readers start depending on them.

| Use this | Not this |
| --- | --- |
| **Changes sync every few seconds.** | The sync service polls the cache every 400 ms and writes to the events table. |
| **The connector retries a failed request.** | The connector retries using exponential backoff in the worker thread pool. |

**Limit.** Some intervals and names are settings the reader can change. Those belong in the documentation.

### Describe failure concretely

When something can fail, say what the reader will see, why it happens, and what to do next. A vague warning is worse than none, because it creates worry without giving the reader an action.

| Use this | Not this |
| --- | --- |
| **If the connector can't reach the sync API for 30 seconds, it saves your changes locally and the dashboard shows a Disconnected status. Check network access to the API endpoint.** | The connector may not always work as expected. |

### Don't promise outcomes

Describe what the product does, not what it will achieve. Results depend on the customer's data, configuration, and usage, so an unqualified promise is one the product can't keep.

| Use this | Not this |
| --- | --- |
| **Recommendations rank the articles most likely to answer the question.** | Recommendations guarantee higher customer satisfaction. |
| **The model ranks possible answers by how closely they match the question.** | The AI always picks the best answer. |

Avoid _always, never, guarantees, ensures,_ and _eliminates_ when you describe what a model does. Prefer _selects, ranks, estimates, predicts,_ and _recommends._

### Keep supported behavior in

Trimming claims doesn't mean trimming facts. If the product does something and it's supported, document it plainly. Removing accurate behavior in the name of caution leaves readers guessing.

## UI text

UI text is the words inside the product: labels, buttons, menus, dialogs, form fields, tooltips, toasts, errors, empty states, and notifications. Someone reads it in the middle of doing something else, so every extra word costs them.

**Limit.** UI strings often live in a string table with keys, placeholder tokens like `{name}`, and character limits you can't see. Never change a key, a token, or anything in code font. If a string looks cut short to fit a limit, flag it rather than lengthening it.

### Quick check for any string

1. Does it say what happens, or what the reader should do?
2. Is it in sentence case?
3. No period on a label or title. A period on a full sentence.
4. Is it the shortest version that still works?
5. No _please, sorry,_ or _oops._

### Capitalization and punctuation in UI

- Sentence case for every label, title, menu item, button, and message.
- No period, colon, or ellipsis at the end of a label, title, menu item, or button.
- A period on any full sentence, even a two-word one. Tooltips and field descriptions take no period unless they run to two sentences.
- A progress message can end with an ellipsis: "Syncing…"
- No exclamation points.

### Buttons

- Lead with the verb that names the action. One word where possible, three at most. A longer action is probably a link.
- Say what happens, not what the control is.
- _Create_ makes something new. _Add_ brings in something that already exists. _Install_ is for software.
- Name the action instead of answering a question. _Yes_ and _No_ are acceptable only when the title is a yes-or-no question and no verb fits. Never _OK_ to confirm an action.

| Before | After |
| --- | --- |
| Submit | Save changes |
| New | Add a project |
| OK | Delete |
| Click here to continue | Continue |

### Dialogs and confirmations

- The title is a question or a statement that names the object: "Delete this project?" Never "Are you sure?" or "Warning!"
- The body states the consequence in one or two sentences: "Its tasks move to your default project."
- Two actions at most. The primary button names the action (Delete, Remove, Discard). The secondary is Cancel. Never OK. Yes and No only when the title is a yes-or-no question and no verb fits.
- A destructive primary button repeats the verb from the title.

| Before | After |
| --- | --- |
| Are you sure? [Yes] [No] | Delete this project? Its tasks move to your default project. [Delete] [Cancel] |

### Error messages

Say what happened, why if the reader can act on the cause, and what to do. Don't blame the reader.

- One message per known cause. "Something went wrong" is the last resort, not the default.
- An error reports a problem that already happened. A warning is about a problem that might. Don't dress an error as a warning.
- No _please, sorry, oops,_ or _unfortunately._
- Passive voice is fine when it keeps blame off the reader: "The password wasn't recognized."

| Before | After |
| --- | --- |
| Oops! We couldn't save your file. | The file didn't save because the disk is full. Free up space and try again. |
| Invalid date | Enter the date as YYYY-MM-DD, for example 2026-03-14. |
| An unexpected error occurred. | The connector lost its link to the sync API. Check network access to the endpoint. |

**Limit.** If the source says what happened but not what to do, and nothing in the source gives the remedy, don't invent one. Flag it: "Error text has no next step."

### Form fields

- The label carries the one instruction the reader needs. A noun or a short noun phrase, in sentence case, with no colon: "Project name."
- Placeholder text disappears when the reader starts typing, so it can never be the only instruction. Use it for an example of the expected input.
- Help text below the field explains a format or a rule the reader can't guess: "Use 8 or more characters." Add it only when getting the input wrong would cause an error.
- Mark whichever kind of field is rarer. If most fields are required, end each optional label with "(optional)." If most are optional, mark the required ones with an asterisk and explain it once at the top of the form. Either way, keep required fields to a minimum.

| Before | After |
| --- | --- |
| Label: none. Placeholder: Enter the project name here | Label: Project name. Placeholder: Website redesign, Q3 launch |
| Label: Email address * (on a form where every field is required) | Label: Email address |
| Label: Phone number. Placeholder: Phone number | Label: Phone number (optional) |

### Tooltips

A tooltip names or briefly describes the control it's attached to. A phrase, not a paragraph. No period unless it runs to two sentences. Don't put anything essential in a tooltip, because keyboard and touch users may never see it.

> Filter by project
>
> Export the current view as CSV

### Toasts and notifications

- One line. It confirms something that already happened or reports something that needs attention.
- One action at most, and Undo is the best one. No links inside the text.
- If it needs two actions, or the reader must deal with it before continuing, it's a dialog, not a toast.

| Before | After |
| --- | --- |
| Your changes have been successfully saved to the system! | Changes saved. |
| The project was deleted. Click here to undo or here to view projects. | Project deleted. [Undo] |

### Success messages

Name what happened. Past tense, one line, no exclamation point.

> Project saved.
>
> Report sent to 3 recipients.

### Empty states

An empty state says why there's nothing here, then what to do. A first-use state ("No projects yet") and a no-results state ("No projects match this filter") are different and shouldn't share a string.

| Before | After |
| --- | --- |
| No items. | No projects yet. Add a project to start tracking work. |
| Nothing found. | No projects match "sales". Clear the filter or try another name. |

**Limit.** If the source has no next action and you don't know what it is, flag it.

### Links

Link text names the destination or the result. Never "click here," and never "learn more" on its own.

| Before | After |
| --- | --- |
| Click here to view the sharing rules. | View the sharing rules. |
| Learn more | Learn more about recommendations |

### Accessibility text

- Every icon-only control needs a text label that a screen reader can announce. Name the action: "Close," "Filter," "Refresh."
- Alt text for an informative image says what it shows or does, not that it's an image. A decorative image gets empty alt text.
- Don't rely on color alone. "The red status" means nothing to a screen reader. Name the state.
- Don't rely on position. "The button on the left" or "see below" breaks when the layout changes or a screen reader reads the page in order. Name the control, or link to the section.

### Interaction verbs

These describe an action without assuming a mouse, a finger, or a keyboard.

| Verb | Use for |
| --- | --- |
| **Open** | Apps, menus, files |
| **Close** | Apps, panes, dialogs, windows, files |
| **Go to** | A place in the UI, such as a tab, a page, or a menu |
| **Select** | Options, values, links, menu items, buttons |
| **Clear** | Unchecking a checkbox |
| **Enter** | Typing a value |
| **Press** | A key or key combination, such as Enter or Ctrl+S |
| **Turn on, turn off** | A toggle or a setting |

Avoid _click_ and _tap._ Each assumes one input device.

| Element | Preposition |
| --- | --- |
| dialog, pane, list, box, window | in |
| tab, page, menu, toolbar | on |

### Naming a label inside a UI sentence

Match the label exactly and let its capitalization set it apart. Don't bold it. Use quotation marks only when the label would otherwise be unreadable in the sentence.

> Select Save changes to keep your edits.
>
> Move the task to the "Needs review" column.

### First person in UI

_You_ is the default. _Me_ and _my_ are fine in a label where the reader is the speaker: "Keep me signed in," "Email me when someone mentions me." Use **My tasks** only when there's also a shared view to tell it apart from. Don't mix _my_ and _your_ on one screen.

### Third-party brands in UI

Use the exact casing from the brand table in [Third-party brands and trademarks](#third-party-brands-and-trademarks). Whether a symbol appears depends on the surface, not on which occurrence comes first.

| Surface | Rule |
| --- | --- |
| **Functional UI:** labels, menus, settings, status, errors, tooltips, connector names | No symbol. Correct casing only. |
| **Legal, About, or third-party notices screen** | The attribution line: "All product and company names are trademarks or registered trademarks of their respective owners." Symbols only where the owner's guidelines require them. |
| **Marketing surfaces inside the product:** an onboarding screen, an integration catalog tile, a "Connect to X" landing page | One symbol, on the screen's title or heading, per the brand table. Not in body text or buttons. |

**Limit.** If the source strings already carry symbols, keep them and flag them for a decision.

### Localization

- Keep strings short. Translations often run 30 to 40 percent longer than English.
- Don't build a sentence from fragments joined at runtime. Word order changes across languages.
- Don't hard-code a date, time, or number format into a string. The platform supplies the format for each locale.
- Leave placeholder tokens such as `{count}` or `%s` exactly as written.

## Documentation

Documentation is prose about the product: feature guides, deployment guides, runbooks, release notes, API references, and help articles. Someone reads it when they're stuck or about to make a decision. Accuracy comes first, brevity second.

### UI labels in documentation

Bold the label, and copy it exactly as the screen shows it, capitalization included.

> Select **Export**.
>
> On the **Sharing** tab, select **Invite people**.
>
> Clear the **Send email notifications** checkbox.

- Use bold for UI labels and run-in headings only. Never for emphasis.
- Prefer describing the action to naming the control. "Save a copy of the report" needs no bold.
- Don't name the control type unless it prevents confusion.
- If the source writes **Export As**, keep **Export As**, even though a new label would use sentence case. The label on the screen is the fact.
- Drop a label's trailing colon or ellipsis.
- A paragraph with more than two or three bold labels should be a numbered procedure.

### Formatting conventions

| Element | Format | Example |
| --- | --- | --- |
| **UI labels** | Bold, exact capitalization | Select **Export**. |
| **Menu paths** | Bold labels joined by a spaced greater-than sign, which isn't bold | Select **Settings** > **Members** > **Invite**. |
| **Commands, code, file names, paths, parameters, and anything typed into a terminal** | Code style. Don't edit what's inside. | Run `git status`. Open `config.yaml`. |
| **Placeholders in code** | A descriptive name in angle brackets. Say what to replace it with. | `sync --project <project-id>` |
| **Keys and shortcuts** | Key names as printed on the keyboard, joined by a plus sign with no spaces. Give each platform's version when they differ. | Press Ctrl+S (Windows and Linux) or Cmd+S (macOS). |
| **A new term being defined** | Italic on first use | A _workspace_ holds all of a team's projects. |
| **Quoted error text** | Quotation marks, exact wording | If you see "Sync paused," check your connection. |
| **File formats** | The format in capitals, the extension in code style | Export a CSV file. The file ends in `.csv`. |

### Headings

- Use sentence case.
- One top-level heading per page: the title. Don't skip levels. A third-level heading sits under a second-level heading, not directly under the title.
- Front-load the words a reader would scan for.
- Start a task heading with a verb ("Invite people"). Use a noun phrase for a concept heading ("Permissions").
- Keep headings at one level parallel.
- Don't stack two headings with no text between them. If you're editing, flag it rather than inventing text.
- Don't introduce an acronym in a heading.
- Avoid ampersands and plus signs.
- No period at the end. A question mark is fine when the heading asks the reader's question.

### Procedures

- Before step 1, say what the reader needs: a role or permission, a version, or something that must already exist.
- Number the steps.
- One action per step. Combine only short actions that happen in the same place. Never reorder steps.
- Start each step with a verb. If the reader needs to know where they are first, lead with the location: "On the **Sharing** tab, select **Invite people**."
- Put a condition before the action: "If you use single sign-on, select **Use SSO**."
- Start an optional step with "Optional:".
- Write full sentences, with a capital letter and an ending period.
- Include the step that finishes the job, such as selecting **Apply**. If you're editing and the source has no finishing step, flag it. Don't add one.
- State the result of a step when it isn't obvious: "The project opens in a new tab."
- Keep a procedure to about seven steps. Split a longer one at a natural pause, such as after saving.
- A single-step procedure uses a bullet, not a number.
- Give the procedure a heading that says what it accomplishes. Skip an introductory sentence that repeats the heading.

> **Invite someone to a project**
>
> 1. Open the project, and select **Share**.
> 2. In **Email address**, enter the person's email address.
> 3. Optional: In **Message**, add a note.
> 4. Select **Send invite**.

### Lists

- Use a bulleted list for items in no particular order and a numbered list for a sequence.
- Two to seven items. If you're editing a longer list, don't cut items. Split it under subheadings, or flag it.
- Keep items parallel: all noun phrases, or all verb phrases.
- Introduce a list with a heading, a full sentence, or a fragment that ends in a colon.
- Start each item with a capital letter.
- End items with periods only when they're full sentences or complete the lead-in sentence.
- No semicolons, commas, or conjunctions at the ends of items.

**Use bullets for dense status lists.** A paragraph that carries several comma-separated states, limits, or options is hard to read. Break it out as a term list: a bold term, a period, and a definition. Keep every item and every definition as written.

| Before | After |
| --- | --- |
| A build can be pending, which means it's waiting for a runner, running, which means it's in progress, failed, or succeeded. | **A build has one of four statuses:**<br><br>- **Pending.** It's waiting for a runner.<br>- **Running.** It's in progress.<br>- **Failed.**<br>- **Succeeded.** |

In the after, _Failed_ and _Succeeded_ have no definitions because the source gave none. Don't write one.

### Tables

- Use a table for data with two or more attributes. For a plain list of similar things, use a list.
- Identify the row in the leftmost column.
- Use sentence case in headers and cells, except for code values and identifiers, which keep their case.
- Make column headers specific. "Employee" or "Group," not "Name."
- Never leave a cell blank to mean "nothing here." Write _None_ or _Not applicable._ If you're editing and don't know which, flag it.
- Introduce a table with a full sentence ending in a period, not a colon.
- Repeat the header row on every page of a long table.

### Notes and warnings

Use them sparingly. A page full of callouts trains readers to skip them.

- **Note:** helpful information that isn't required to finish the task.
- **Important:** information the reader needs to succeed.
- **Warning:** a risk of data loss, a security exposure, or downtime. Say what happens and how to avoid it.

Don't stack two callouts, and don't put a step inside one.

### Links in documentation

- Link text names the destination: "See [Permissions](#)." Not "click here."
- Don't link the same destination more than once in a section.
- For a cross-reference, use the exact title of the section or page.
- Don't point with "above" or "below." Link to the section by name.

### Screenshots and alt text

- Crop a screenshot to the part the reader needs.
- Don't rely on a screenshot alone for a step. The text must work without it.
- Use fictional data. No real customer names, email addresses, or account details.
- Give every informative image alt text that says what it shows. Don't start with "Image of."
- When the UI changes, update the screenshot or remove it. A stale screenshot misleads more than no screenshot.

### Release notes

- Write one entry per change the reader can notice. Leave out internal work unless it changes behavior.
- Group entries under fixed headings in a fixed order: New, Changed, Fixed, Deprecated, Removed, Security. Skip a heading with no entries.
- Start each entry with what changed, from the reader's side: "Exports now include archived projects." Not the ticket number, the team, or the pull request.
- Say what the reader must do, if anything, and by when: "Update the connector to version 2.3 before March 1, 2027."
- Name the version and date every release. Spell out the month.
- Keep thanks, celebration, and apology out of the entries. They belong in the announcement, if anywhere.

### API reference

- Write the HTTP method in capitals and the path in code style: `GET /projects/{id}`.
- Start an endpoint's description with a present-tense verb: "Returns the project." "Creates a task."
- For every parameter and field, give the name in code style, the type, whether it's required, the default, and one sentence on what it does. Use the same column order in every table.
- Show one complete request and one complete response, with realistic but fictional values. Make sure the example is valid.
- Document every error the caller can receive, with its code and what to do about it. Leave out errors the caller can't act on.
- Use one name for one thing. If the field is `project_id`, the prose doesn't call it the project key.

### Code samples

- Make every sample run, and test it again when the product changes.
- Mark placeholders so nobody copies them into production: `<your-api-key>`, `example.com`, `user@example.com`.
- Never paste a real key, token, password, internal hostname, or customer record, not even an expired one.
- Show the expected output when it helps the reader confirm success.
- Keep the sample to the point being made. Leave out setup the reader already did.
- Name the language or shell, and keep one convention across the document.

### Cut the fluff

These are the most common review findings. Each adds length and no information.

| Cut this | Because |
| --- | --- |
| "The table below shows the supported connectors." | The table is right there |
| "This section explains how to configure notifications." | The heading already said so |
| "In today's fast-paced digital world ..." | Says nothing |
| "It is important to note that ..." | State the thing |
| A closing paragraph that restates the opening | The reader already read it |

**Limit.** Cut a sentence only if every fact in it appears in the heading or in the next sentence. "This section explains how to configure notifications for shared projects" carries a scope ("shared projects") that the heading may not. Move the fact, then cut.

## Numbers

Copy a number that appears in the UI exactly as the UI shows it. Never reformat an identifier, a version string, or a code value. Otherwise, follow these rules.

### Numerals or words

| Situation | Write | Example |
| --- | --- | --- |
| **Prose, 0 through 9** | The word | five projects |
| **Prose, 10 and up** | Numeral | 12 members |
| **UI, tables, tight space** | Numeral, any size | 5 projects |
| **Several numbers of the same kind in one sentence** | Numerals throughout | The release has 14 fixes, 3 new features, and 2 known issues. |
| **Start of a sentence** | Never a numeral. Spell it out or rewrite. | Eleven projects are active. |
| **Measurements and durations** | Numeral, even below 10 | 3 seconds, 5 minutes, 0.75 GB, 80 × 80 pixels |
| **Time of day** | Numeral plus AM or PM, or 24-hour time if the product uses it | 10:45 AM, or 22:45. Write _noon_ and _midnight,_ not 12:00. |
| **Percent in prose** | Numeral plus _percent_ | 50 percent |
| **Percent in UI and tables** | Numeral plus % | Resolved: 87% |

### Commas in numbers

Use a comma from four digits: 1,024. Don't use one in years (2026), after a decimal point, or in version numbers, port numbers, and identifiers (port 8080).

### Units

Put a space between a number and its unit: 25 MB, 5 GB, 30 ms. No space before a percent sign: 87%. The unit is plural for anything that isn't exactly 1: 0.5 seconds, 1 second, 5 seconds.

### Dates and times

- Spell out the month. 6/12/2026 means two different dates depending on the reader's country. Write _June 12, 2026._
- Don't use ordinals in dates. _June 1,_ not _June 1st._
- In data formats, logs, and code, use the ISO form: 2026-06-12.
- Give a time zone when readers in other zones will see the time: 9:00 AM UTC.
- Name a month or a quarter, not a season. Seasons differ by hemisphere.

### Ranges

- In prose, write _from 5 through 50._
- In tables and UI, use an en dash with no spaces: 2016–2026.
- For times, use _to:_ 10:00 AM to 2:00 PM.
- Don't put _from_ before an en dash range.

### Large numbers

In prose, write _1.2 million._ In tight UI, _K, M,_ and _B_ are fine: capitalized, with no space (12K). Don't use a decimal with _K_ unless it saves space.

### Other numbers

- **Decimals.** Use a leading zero below one: 0.5.
- **Negative numbers.** Use a minus sign (−), not a hyphen or an en dash.
- **Ordinals.** Spell out _first_ through _ninth._ Don't write _firstly._
- **Versions.** Write them as the product publishes them: _version 4.2,_ `v4.2.1`.
- **Phone numbers in examples.** Use numbers reserved for fiction, such as 555-0100 through 555-0199 in North America.

## Punctuation

If a sentence needs more than a comma or two and an end mark, it's probably two sentences.

### Periods

- End every full sentence with a period, even a two-word one.
- Use one space after a period.
- No period on headings, titles, UI labels, or list items that aren't full sentences.

### Commas

- Use the serial comma in a list of three or more: _chat, email, and video._
- Use a comma after an introductory phrase: "On the **Sharing** tab, select **Invite people**."
- Use a comma before _and, but,_ or _so_ when they join two full sentences.
- Don't put a comma between two verbs that share one subject: "The connector retries the request and logs the result."
- If a series is long or its items contain commas, use a bulleted list.

### Colons

- Use a colon to introduce a list, inline or bulleted, when the lead-in is a full sentence or needs the items to finish it.
- Don't use a colon to attach an explanation to a sentence. Write two sentences.
- After a colon in a sentence, lowercase the next word unless it's a proper noun. In a heading or title, capitalize it.
- Never end a heading or a UI label with a colon.

### Semicolons

Don't use them. Readers rarely see semicolons outside formal writing, and a sentence that needs one is usually two sentences or a list.

| Before | After |
| --- | --- |
| The sync finished; three files were skipped. | The sync finished. Three files were skipped. |

### Dashes

**Em dash (—).** Don't use it. Readers now associate the em dash with machine-written text, and every job it does has a clearer replacement.

| The dash was doing this | Use this instead | Example |
| --- | --- | --- |
| **Setting off a definition or an aside** | A pair of commas | The export, a CSV file with one row per task, downloads automatically. |
| **Introducing a list** | A colon | Each task has three dates: created, due, and closed. |
| **Adding an aside the sentence could drop** | Parentheses | Sync runs every 15 minutes (or right away, if you select **Sync now**). |
| **Explaining, or joining two related statements** | A period, and two sentences | Keep procedures short. Seven steps is a good limit. |
| **Marking an abrupt turn** | A rewrite | Rework the sentence so the turn isn't needed. |

**En dash (–).** Use it for number and date ranges, with no spaces: 2016–2026. In a UI time range, spaces are fine: 2:15 PM – 4:45 PM. Don't use it as a minus sign.

**Minus sign (−).** Use it for negative numbers and subtraction: −12, 10 − 3 = 7.

### Hyphens

- Hyphenate a compound modifier before a noun, and leave it open after the noun: _a well-known issue,_ but _the issue is well known._ Also _a 30-day trial, real-time updates,_ but _updates in real time._
- Don't hyphenate after an adverb ending in _-ly:_ _a newly created project._
- Most prefixes take no hyphen: _autoscale, preview, rerun, nonzero, multifactor._
- Hyphenate when the word would be misread without one (_re-create, re-sort_), or when the next character is a capital letter or a numeral (_non-English, pre-2020_).
- Spell out both parts instead of suspending a compound. Write _first-level and second-level headings,_ not _first- and second-level headings._
- It's _email,_ not _e-mail._

### Apostrophes

- Add _'s_ to make a singular noun possessive, even one ending in _s:_ _the process's ID._ Add only an apostrophe to a plural ending in _s:_ _the members' roles._
- Don't use an apostrophe to make a plural: _APIs, 2020s._
- Don't make a product name possessive. See [Plurals and possessives](#plurals-and-possessives).

### Quotation marks

- Use straight quotation marks (" "), not curly ones. They render the same in every font, browser, and code editor.
- Put periods and commas inside the closing quotation mark. Put other punctuation outside unless it's part of the quoted text.
- **Exception:** when the quoted text is a literal value, such as a search term or a file name, put the punctuation outside so it isn't read as part of the value: No projects match "sales".
- Use single quotation marks only for a quotation inside a quotation.
- Don't use quotation marks for emphasis.

### Parentheses

- Use parentheses for an aside the sentence could drop. If the reader needs it, it doesn't belong in parentheses.
- Don't nest them.
- Put the period inside only when the whole sentence is in parentheses.

### Ellipses

- Don't end a UI label with one, and drop it when you name a label in documentation.
- A progress message can end with one: "Syncing…"
- In a quotation, an ellipsis marks omitted text.

### Exclamation points and question marks

- Don't use exclamation points in UI or documentation.
- Use a question when the reader has a decision to make ("Delete this project?") or in a heading that asks the reader's own question.

### Slashes

- Use a slash only for a fixed pair: _on/off, read/write, client/server._
- Don't use a slash in place of _or._ "Select a project/task" becomes "Select a project or a task."
- A slash (/) separates folders in URLs and in macOS and Linux paths. A backslash (`\`) separates them in Windows paths. In cross-platform documentation, use forward slashes, or show each platform's path.

### Ampersands

Use _and._ Keep an ampersand only when it's part of a name or a UI label.

### Punctuation next to formatting

Punctuation takes the style of the sentence, not the label. In "Select **Save**, and then close the tab," the comma isn't bold. In "Select **Settings** > **Members**," the greater-than sign isn't bold.

## Inclusive language

Software reaches people everywhere. Content that excludes people is a defect.

### Pronouns in generic references

Don't use _he, him, his, she, her,_ or _hers_ for a generic person. In order of preference:

1. Rewrite to _you._
2. Rewrite to a plural.
3. Use _the_ or _a_ instead of a pronoun.
4. Name the role: _the admin, the reviewer, the customer._
5. Use singular _they_ when nothing else works.

Never write _he/she_ or _s/he._

| Before | After |
| --- | --- |
| If the user has the right permissions, he can reset other users' passwords. | If you have the right permissions, you can reset other people's passwords. |
| A reviewer sees his own tasks on the home screen. | Reviewers see their own tasks on the home screen. |

Use the pronouns a real person uses. Gendered pronouns are correct for a named person who uses them and in direct quotations.

### Gender-neutral words

| Write | Instead of |
| --- | --- |
| **chair, moderator** | chairman |
| **staff, workforce** | manpower |
| **sales representative** | salesman |
| **staffed** | manned |
| **people, humanity** | mankind |
| **artificial, synthetic** | man-made |

### Terms that carry bias

| Write | Instead of |
| --- | --- |
| **primary, secondary** | master, slave |
| **main** (branch) | master (branch) |
| **blocklist, allowlist** | blacklist, whitelist |
| **legacy, exempt** | grandfathered |
| **quick check, confidence check** | sanity check |
| **placeholder, sample** | dummy |
| **stop responding** | hang |

**Limit.** A term that's part of a command, a setting, or an API stays as written. Flag it if it should change in the product.

### Combat and violence metaphors

Don't borrow language from combat when you mean something ordinary.

| Write | Instead of |
| --- | --- |
| **address, prevent, respond to** | combat, fight, eliminate |
| **threat actor** | adversary |
| **impact, scope** | blast radius |
| **attack sequence** | kill chain |
| **customer-facing** | frontline |
| **delete, reset** | nuke |
| **incident room** | war room |
| **reliable** | bulletproof |

Also avoid _strike_ and _troops._ A technical term such as the `kill` command stays as written.

### Disability

Focus on people, not conditions: _people who are blind or have low vision,_ not _the blind._ Write _uses a wheelchair,_ not _wheelchair-bound._ Don't use _stricken with_ or _suffering from._ Don't mention a disability unless it matters to the point.

Don't use a disability as a metaphor. "The outage crippled the service" becomes "The outage stopped the service." "Blind to the risk" becomes "unaware of the risk."

### Race and ethnicity

Capitalize the names of racial and ethnic groups: Asian, Black, Hispanic, Indigenous, Latino, Native American, Pacific Islander. Lowercase _white_ and _multiracial._ Use the term a group uses for itself, and mention race or ethnicity only when it's relevant.

### Age

Don't use age as shorthand for skill. "So easy your grandparents can use it" becomes "Easy to set up."

### Examples and scenarios

- Use names from a range of cultures and gender identities, and vary who holds which job.
- Don't assume a Western or affluent setting.
- Don't name politically disputed places.
- Don't generalize about groups, including flattering generalizations.
- Avoid slang and anything that could read as cultural appropriation, such as _spirit animal_ or _tribe_ for a team.

### Products aren't people

Don't give products human qualities. They don't think, feel, want, or decide. This matters most for AI features, where the language invites it. A model _ranks, selects, estimates, predicts,_ and _recommends._ It doesn't _understand, believe,_ or _know._

When you're editing someone else's text and it says a product thinks or knows, flag it and suggest a verb. Don't rewrite the claim yourself.

## Writing for a global audience

Many readers speak English as a second language, and many read your text through a translation tool. Text that's clear to them is clearer for everyone.

- **One idea per sentence.** Short sentences translate better.
- **Keep _that_ when it helps.** "Make sure that the sync finished" is easier to parse than "Make sure the sync finished."
- **Avoid idioms and sports metaphors.** "Out of the box" becomes "by default." "A ballpark figure" becomes "a rough estimate."
- **Avoid Latin abbreviations.** See the [word list](#word-list).
- **Spell out months, and name quarters instead of seasons.** See [Dates and times](#dates-and-times).
- **Name the currency:** 25 USD, or US$25.
- **Avoid acronyms that look like words,** because a translation tool may translate them.
- **Keep text out of images.** Text in an image can't be translated or read by a screen reader.

For UI strings, also see [Localization](#localization).

## Text that sounds machine-written

Readers notice text that sounds generated, and they trust it less. These patterns are the usual giveaways.

- **Em dashes.** The strongest tell. See [Dashes](#dashes) for replacements.
- **Semicolons.** Split the sentence or make a list.
- **A colon in the middle of a sentence** that introduces an explanation instead of a list.
- **"It's not just X, it's Y."** Say what it is.
- **Openers that announce.** "In today's fast-paced digital world."
- **Sentences that introduce the next thing.** "The table below shows the supported connectors."
- **Stacked hedges.** "It's generally usually best to typically avoid." One hedge that states a real limit can stay.
- **Filler intensifiers.** _Genuinely, actually, literally, truly, really._
- **_Moreover, Furthermore,_ and _Additionally_** chaining paragraphs together.
- **A punchy one-liner after every point.**
- **Bold scattered through prose** for emphasis.
- **A closing paragraph that restates the opening,** when it adds no fact.

## Reviewing a draft

### Review order

Work in this order. Each pass looks for one kind of problem.

1. **Claims.** Flag anything unreleased, internal, without a remedy, or overpromised. See [Writing about product behavior](#writing-about-product-behavior).
2. **Terminology.** Product names, brand casing and symbols, defined terms, _the user,_ and any word that could mean either the product or the category.
3. **Machine tells.** Em dashes and semicolons first, then the rest of [Text that sounds machine-written](#text-that-sounds-machine-written).
4. **Structure.** Heading case, bullets for dense lists, parallel lists, and sentences that only announce. For UI text, check each string against its component's rules.
5. **Proofreading.** The sweep below.
6. **Fidelity.** Compare before and after. Every number, name, date, version, step, condition, key, and token is unchanged. Nothing was added. Nothing that carried a fact was deleted.

If you're reviewing several documents, decide each terminology question once and apply it to all of them.

### Proofreading sweep

Read the whole draft once for each line.

- **Spelling.** Misspellings. US spelling (_color, organize, center_). The same spelling of every term every time. Homophones a spell-checker misses (_their/there, its/it's, affect/effect, then/than, lose/loose_).
- **Doubled and dropped words.** "the the," "to to," or a missing _a_ or _the_ left behind by an edit.
- **Agreement.** Subject with verb, and pronoun with noun, especially across a long subject or a list.
- **Tense drift.** A stray _will_ or _was_ in present-tense text that isn't about the future or the past.
- **Dangling modifiers.** "After saving the file, the dialog closes." The dialog didn't save anything.
- **Awkward phrasing.** Read the draft aloud. Rewrite any sentence you had to read twice, without changing what it says.
- **Punctuation.** Serial comma. Straight quotation marks. No period on headings or labels. No em dashes. No semicolons.
- **Capitalization.** Sentence case on headings. UI labels match the screen. Defined terms are consistent.
- **Numbers.** Words below 10 in prose, numerals in UI, commas from four digits, _percent_ in prose and % in tables. Identifiers and versions untouched.
- **Links and cross-references.** Every link goes somewhere. Every "see X" names a section that exists.

### Quick reference

For a one-page checklist, see [The short version](#the-short-version).
