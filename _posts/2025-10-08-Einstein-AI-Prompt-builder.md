---
layout: post
title: Field Generation Prompt Template with Einstein Generative AI
image: "/posts/primes_image.jpeg"
tags: [Einstein Generative AI, Prompt Template, Field Generation]
---

---

The scenario centers on a familiar challenge: managing customer support cases. To enhance productivity and improve customer satisfaction, you’ll leverage generative AI to create concise, 100-word summaries of case details. These AI-generated summaries help agents get up to speed faster and make it easier to spot cases that require extra attention.

**Create a prompt template**

In Setup → Prompt Builder, click New Prompt Template.

Choose Field Generation as the template type.

Give the template a name and description (e.g. “Quick Summary”).

Associate it to the Case object and a specific text field (e.g. Quick_Summary). 
Trailhead

Now, write your instructions. The example provided:

```ruby
“Summarize the concatenation of the contents of the comment bodies of COMMENTS along with the text from SUBJECT, the case priority which is PRIORITY, and the case type which is TYPE. Keep the response to a single short paragraph.”
```

You’ll then replace placeholders like COMMENTS, SUBJECT, PRIORITY, and TYPE with merge fields (i.e. Input:Case.CaseComments, Input:Case.Subject, etc.). This lets the prompt pull in real data dynamically.

Finally, select which LLM model to use (for example, OpenAI GPT-4 Omni Mini) and save.

```ruby
**To make the summary field accessible in the UI:**

- Edit the Case Lightning page and upgrade to Dynamic Forms (if not already).

- For the Quick Summary field, set its Prompt Template to the one you created.

- Save and activate that page configuration.
```

Once live, users will see a prompt icon beside the field — click it, and Einstein will suggest a summary based on your template. They can accept the suggestion (or iterate further) and then save it.

Amazing!




