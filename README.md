
# PAYME.yaml

An open source, standardized file format for open source projects to declare how
to financially support their contributors.

### How to use

To accept money for your open source project, simply add a `PAYME.yaml`
file in the root of your repository and add ways that you would like to be paid.

```yaml
paypal: email@example.com
bitcoin: long-address-here
# etc
```

### FAQ


#### How will this file fund open source projects?

This specification is a small piece in a very complex ecosystem 


#### Why not GitHub Sponsors?
[GitHub Sponsors](https://github.com/sponsors) is a funding model for
projects hosted on GitHub.

PAYME.yaml is **not** a funding model, it is a standardized format
for developers to declare *by what means* they would like to be
compensated for a particular project.

It is more appropriate to compare the `PAYME.yaml` file format with
GitHub's `.github/FUNDING.yml` file format.


#### Why not just use `.github/FUNDING.yml`?
`.github/FUNDING.yml` is a closed-source, centralized standard.
The standard of open source funding should be open source.

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


Regardless, `PAYME.yaml` is a superset of the current
`.github/FUNDING.yml` format, so you can also simply get
the best of both worlds and create a symlink between the two.


#### Why `.yaml` and not `.yml`?
The [YAML specification](https://yaml.org/faq.html) has made
it clear that the preferred extension is `.yaml` since 2006.
This project recommends that parsing clients first look for `PAYME.yaml`,
falling back on `PAYME.yml` if necessary.
