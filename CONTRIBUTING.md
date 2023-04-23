# Contribution Guidelines

Please note that this project is released with a [Contributor Code of Conduct](CODE_OF_CONDUCT.md).
By participating in this project you agree to abide by its terms. You'll be also asked to agree to
[the Linux DCO](https://developercertificate.org) by signing-off your commit/contributions.[^1]

## Contributing via GitHub (or GitLab via `mau.dev`)

The easy way to contribute to the list is by filing a new issue with the [Submit a resource issue form](https://github.com/Community-Lores/awesome-neurodiversity/issues/new?assignees=ajhalili2006&labels=enhancement%2Cdocumentation&template=suggest-resource.yml)
(or template in `mau.dev`).

## Contributing via sourcehut (email patches + todo.sr.ht)

We also use [sourcehut](https://sourcehut.org) to [track issues](https://todo.sr.ht/~ajhalili2006/awesome-neurodiversity) and also accept email patches at `~ajhalili2006/awesome-neurodiversity-devel@lists.sr.ht` ([archive](https://lists.sr.ht/~ajhalili2006/awesome-neurodiversity-devel)).[^3]

To make our lives easier for regular contributors over email, an addition of these configs into your local copy of the repository should save you time when handing out patches out in the wild.

```bash
# Please avoid emailing the maintainers personally for patches, that's bad pratice in OSS community.
git config sendemail.to "~ajhalili2006/awesome-neurodiversity-devel@lists.sr.ht"

# We also need signoff too in compliance with Linux DCO.
git config format.signoff true
```

### Template

```md
<!--

GitHub user? We do use issue forms instead of painfully editing Markdown files. Go to the GitHub mirror's
issue tracker, select "New issue" and choose Suggest a resource.

While sourcehut's Markdown renderer doesn't support checkboxes yet, we still need it once we enabled issue tracker mirroring between services in the future.
To tick a box for starters, just replace [ ] with [X] and vice versa.

-->

### Link to resource

<!-- 

Please paste the URL where that resource you're suggesting is available over the internet. If it's a book, an Amazon URL is fine.

--->

### Type of resource

<!--

For details on different types as listed below, please see the contributing guidelines within the repository but they're self-explanatory by the way.

-->

- [ ] Website / Webpage
- [ ] Blog post
- [ ] Book / Audiobook
- [ ] Video
- [ ] Podcast
- [ ] Online Course
- [ ] Community
- [ ] Essay
- [ ] Social Media Post


### Availability to public

<!--

Whenever this is available to public without any restrictions or not.

When picking a option, just tick one. When unsure, leave anything unticked and we'll note it.

-->

- [ ] Free for all
- [ ] Free for all, but login required
- [ ] Free for all, but protected by DRM
- [ ] Behind gated paywall
- [ ] Requires paid access
- [ ] Behind paywalls/Requires paid access + protected by DRM

### Any content warnings?

<!--

If the content you provided contains parts that might be triggering to some, please label it as such.

If chose "None of the above", make sure no other options are ticked.

-->

- [ ] Discrimination (e.g. homophobia, ableism, etc.)
- [ ] Discussions around mental health and trauma
- [ ] Abuse (e.g. child/sexual abuse, ABA)
- [ ] Suicide
- [ ] Others (note it in additional details)
- [ ] None of the above

### Which neurotypes does this resource apply to?

<!--

Select all that apply to help with categorization.

-->

- [ ] Autism
- [ ] ADHD
- [ ] Bipolar
- [ ] PTSD / CPTSD
- [ ] Dyslexia
- [ ] Dyscalculia
- [ ] Epilepsy
- [ ] Schizophrenia
- [ ] OCD
- [ ] TBI
- [ ] Tourette Syndorome
- [ ] Plurality
- [ ] Misc Neurodivergent

### Additional details

<!--

Help us review this suggestion throughly by providing us some context or even a bit of summary.

-->

```

## Updating your merge request

A lot of times, making a MR adhere to the standards above can be difficult.
If the maintainers notice anything that we'd like changed, we'll ask you to
edit your MR before we merge it. There's no need to open a new MR, just edit
the existing one. If you're not sure how to do that,
[here is a guide](https://github.com/RichardLitt/knowledge/blob/master/github/amending-a-commit-guide.md)
on the different ways you can update your MR so that we can merge it.

In case of email patches at sourcehut, an quick `git commit -a --amend` (`-a` for `--all`) should be enough[^2] then `git send-email --annotate -v2 HEAD^` (change `-v2` into intended version number in form of `-v<last version number you sent> + 1`).

[^1]: While I could use Recap Time Squad CLA for this type of documentation project, we don't need to worry about the legalese parts as this might cause first-time contributors headaches.
[^2]: in case you need help with rebasing, see <https://git-rebase.io/> and <https://git-scm.com/book/en/v2/Git-Branching-Rebasing>.
[^3]: To get started with email patches, you need a bit of hands on experience with the command line inteface, especially the `git` commands. If you want to go hardcore, train yourself using Vim (or Neovim). (Otherwise, you can use `nano` or even VS Code.) Go to <https://git-send-email.io/> and follow the tutorial.