# LJT-Homepage

Junteng Liu's personal academic homepage, forked from [Academic Pages](https://github.com/academicpages/academicpages.github.io).

The site reuses only the existing About homepage and Publications page. The About homepage contains the saved personal details, education, research interests, research experience, all six publications, documented research areas under Skills, the Zhiyuan Honor Scholarship, and contact information. Publications are also recorded on the existing Publications page.

Personal and publication information is taken only from the supplied memory. No additional programming skills, photographs, paper URLs, exact publication dates, or biographical claims have been supplied. Template demonstration pages and sample collections are excluded from the site build.

## Site files

- `_pages/about.md`: About homepage and complete profile.
- `_pages/publications.html`: the same six publications.
- `_config.yml`: saved profile details and project-site URL settings.
- `_data/navigation.yml`: About and Publications navigation only.

## Build and deployment

The GitHub Pages project path is `/LJT-Homepage`. The existing GitHub Actions workflows validate and build the site. The validation checks that only the two intended HTML pages are generated and that both contain all six publications, the saved contact links, and working internal links.

The deployment workflow always uploads the built site as a `github-pages` artifact. It deploys when GitHub Pages is enabled and accessible. Initial Pages activation requires repository-administration permission, which the workflow token does not have; in the repository's **Settings > Pages**, the deployment source must be **GitHub Actions**. Until Pages is enabled, the workflow reports this limitation and skips live deployment rather than failing the site build.

For local preview:

```sh
bundle install
bundle exec jekyll serve
```

The Academic Pages theme and its MIT license are retained.
