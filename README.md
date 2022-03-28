
# PAYME.yaml

An open source, standardized file format for open source projects to declare how
to financially support their contributors.

## How to use

To accept money for your open source project, simply add a `PAYME.yaml`
file in the root of your repository and add ways that you would like to be paid
(use the [official example](PAYME.example.yaml)).

```yaml
paypal: email@example.com
bitcoin: long-address-here
# etc
```

Now organizations that use your project know **how** to pay you for your work.

---

### How will this file fund open source projects?

This specification is a small piece in what will be a very complex ecosystem.

Essentially, the future of open source compensation is automation.
Each organization uses tens of thousands of tiny open source projects.
Each open source project could have tens of thousands of users.

`PAYME.yaml` acts as the **interface** between open source contributors
and the organizations that want to give back.

### How do I help contribute to open source sustainability?

Just add a `PAYME.yaml` file to your open source projects!
Even if you don't put anything in it, you'll be helping
proliferate the standard and bring open source closer to sustainability.

And if you *do* put something in it, somebody might just
pay you for all your hard work! 

If you're especially passionate, you can help contribute to the
development of the standard directly. See [CONTRIBUTING.md](CONTRIBUTING.md) for
more information.


### Why not GitHub Sponsors?
[GitHub Sponsors](https://github.com/sponsors) is a funding model for
projects hosted on GitHub.

`PAYME.yaml` is **not** a funding model, it is a standardized format
for developers to declare *by what means* they would like to be
compensated for a particular project.

It is more appropriate to compare the `PAYME.yaml` file format with
GitHub's `.github/FUNDING.yml` file format.


### Why not just use `.github/FUNDING.yml`?
`.github/FUNDING.yml` is a closed-source, centralized standard.
**The standard of open source funding should be open source.**

Paradoxically, the widespread adoption of GitHub Sponsors and
`.github/FUNDING.yml` will make it easier for open source to
sustainably exist, but will also make it more difficult to
sustainably exist without GitHub.

Additionally, GitHub managing both the file format and the funding model
GitHub Sponsors is an undeniable conflict-of-interest. While it is not the
place of this project to accuse GitHub of malicious intent,
leaving the format centralized goes against the spirit of open source.

GitHub has also [made it clear](https://github.blog/2019-06-12-faq-with-the-github-sponsors-team/)
they will not be adding many of the formats that `PAYME.yaml`
supports (such as PayPal) due to a "less explicit social contract".
We think this unnecessarily increases the onboarding cost for getting paid,
particularly for small, single developer projects. 


Regardless, `PAYME.yaml` is a superset of the current
`.github/FUNDING.yml` format, so you can also simply get
the best of both worlds and create a symlink between the two.


### Why `PAYME`?
A standard is only as effective as its adoption.
Put simply, `PAYME` in all caps at the root of a project directory does
not go unnoticed. Word of mouth will be key to widespread usage of `PAYME.yaml`.

For developers, it also increases the likelihood of somebody discovering
your payment preferences and choosing to send some money your way.


### Why `.yaml` and not `.yml`?
The [YAML specification](https://yaml.org/faq.html) has made
it clear that the preferred extension is `.yaml` since 2006.
This project recommends that parsing clients first look for `PAYME.yaml`,
falling back on `PAYME.yml` if necessary.


### How does `PAYME.yaml` handle projects with multiple contributors?
The purpose of `PAYME.yaml` is to standardize **how** money can be sent
to a project, not to standardize what happens to that money after
it has been received.

If you are a single developer project, using the
`paypal:` configuration of `PAYME.yaml` is more than sufficient.
If you require more control over how money is distributed after
receiving, use a purpose-built platform such as [Open Collective](https://opencollective.com/)
along with the `opencollective:` configuration.

### What if I get locked out of my (PayPal, Patreon, etc) account for receiving money?
The `PAYME.yaml` standard suggests that automated clients looking to send money through
`PAYME.yaml` should make the best possible effort to pull the latest copy of `PAYME.yaml`
from the originating git repository's default branch. 

Therefore, as long as your `PAYME.yaml` is kept up to date and is publicly accessible,
losing money to a locked-out account shouldn't happen.

Unfortunately, if your git repo needs to move, it becomes more difficult to push changes.
Proper usage of the `git:` configuration should help mitigate this edge case.

