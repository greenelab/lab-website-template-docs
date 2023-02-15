# Team members

## Add/remove members

To add or remove a team member, create or delete a Markdown file in `/_members`.&#x20;

Each file will automatically generate its own page according to its filename. For example, a file with the name `tim-member.md` will generate a page at `yoursite.com/members/tim-member`.

{% hint style="info" %}
After adding members, you can display them on your site with the [list](../components/list.md) and portrait components.
{% endhint %}

Example:

{% code title="tim-member.md" %}
```markdown
---
name: Tim Member
image: images/team/some-image.jpg
role: programmer
description: Senior Programmer
aliases:
  - T Member
  - T. Member
  - Timothy Member
links:
  home-page: https://tims-website.com/
  email: tim-member@email.com
  twitter: tims_twitter
---

A bio for Tim, written in Markdown.
A descriptions of his academic studies, his recent accomplishments, his goals for the future, his likes/dislikes, etc.
One or two paragraphs is probably best.
```
{% endcode %}

#### Parameters

| Parameter   | Description                           |
| ----------- | ------------------------------------- |
| name        | Display name of team member.          |
| image       | URL to portrait photo of team member. |
| role        |                                       |
| description |                                       |
| aliases     |                                       |
| links       |                                       |

