# OSCIBIO website

This repository contains the source files for the website of the [Atlantic Canada Species At Risk Habitat Modelling Community of Practice](https://atlantichabitatmodels.github.io/communityofpractice/).

## Usage

This website makes use of the static website generator [Jekyll](https://jekyllrb.com/) and the [Petridish](https://github.com/peterdesmet/petridish) theme. **Each commit to `gh-pages` will automatically trigger a new build on GitHub Pages.** There is no need to build the site locally, but you can by installing Jekyll and running `bundle exec jekyll serve`.

Minor changes can be committed directly to `main`.

Changes requiring review (e.g. new blog posts) should be created in a separate branch and submitted as a pull request. Some guidelines:

- Use `72dpi` as image resolution
- Place background images in `assets/images/`, name them after their corresponding page/post and ideally crop them to `2100 x 700px`
- Place content images in `assets/images/`, name them after their corresponding page/post + a suffix, e.g. `-month-tracks-3`
- Add categories to posts to indicate the project, output type, software language, and maybe partner organization, e.g. `[Model Spotlight, SDM, PEI, birds, Species at Risk, Canada Warbler, Olive-sided Flycatcher, Eastern Wood-Pewee]`
- Create internal links as `[previous post]({% post_url 2013-10-01-tracking-eric %})`

## Repo structure

The repository structure follows that of Jekyll websites.

- General site settings: [_config.yml](_config.yml)
- Pages: [pages/](pages/)
- Posts: [_posts/](_posts/)
- Images & static files: [assets/](assets/)
- Top navigation: [_data/navigation.yml](_data/navigation.yml)
- Footer content: [_data/footer.yml](_data/footer.yml)
- Team members: [_data/team.yml](_data/team.yml)

## License

This work is licensed under a [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/).