---
title: Overview of Projects
description: Python packages and tools that makes life a little easier. Get access to the source code and documentation for each project here.
hide:
  - navigation
---

# GitHub Projects
## Browserist 👨‍💻
Python extension for the Selenium web driver that makes browser automation even easier.

[![Downloads](https://static.pepy.tech/badge/browserist)](https://pepy.tech/project/browserist)
[![Browserist source code on GitHub](https://img.shields.io/static/v1?label=GitHub&message=source%20code&logo=github&color=teal&link=https%3A%2F%2Fgithub.com%2Fjakob-bagterp%2Fbrowserist)](https://github.com/jakob-bagterp/browserist/)

[Go to documentation](https://jakob-bagterp.github.io/browserist/){ .md-button .md-button--primary }

## Colorist for Python 🌈
Lightweight Python package that makes it easy and fast to print colored text in the terminal.

[![Downloads](https://static.pepy.tech/badge/colorist)](https://pepy.tech/project/colorist)
[![Colorist source code on GitHub](https://img.shields.io/static/v1?label=GitHub&message=source%20code&logo=github&color=teal&link=https%3A%2F%2Fgithub.com%2Fjakob-bagterp%2Fcolorist-for-python)](https://github.com/jakob-bagterp/colorist-for-python/)

[Go to documentation](https://jakob-bagterp.github.io/colorist-for-python/){ .md-button .md-button--primary }

## IndexNow for Python 🔎
Package that makes it easy to submit URLs to the IndexNow API of Bing, Yandex, DuckDuckGo, and other search engines.

[![Downloads](https://static.pepy.tech/badge/index-now-for-python)](https://pepy.tech/project/index-now-for-python)
[![IndexNow for Python source code on GitHub](https://img.shields.io/static/v1?label=GitHub&message=source%20code&logo=github&color=teal&link=https%3A%2F%2Fgithub.com%2Fjakob-bagterp%2Findex-now-for-python)](https://github.com/jakob-bagterp/index-now-for-python/)

[Go to documentation](https://jakob-bagterp.github.io/index-now-for-python/){ .md-button .md-button--primary }

### Action to Automatically Submit URLs and Sitemap to IndexNow 🤖
Based on [IndexNow for Python](https://jakob-bagterp.github.io/index-now-for-python/), this action can automatically submit your URLs and sitemap to IndexNow for faster indexing by Bing, Yandex, DuckDuckGo and other search engines.

If you're already using GitHub Actions, it's straightforward to incorporate it into your project. The [following workflow will automatically submit the URLs from your sitemap](https://jakob-bagterp.github.io/index-now-submit-sitemap-urls-action/) at regular intervals, such as once a month:

```yaml linenums="1" title=".github/workflows/submit_sitemap_to_index_now.yml"
name: Submit Sitemap to IndexNow

on:
  schedule:
    - cron: 0 0 1 * *  # Run at midnight UTC on the 1st day of each month.

jobs:
  submit-sitemap:
    runs-on: ubuntu-latest
    steps:
      - name: Submit sitemap URLs to IndexNow
        uses: jakob-bagterp/index-now-submit-sitemap-urls-action@v1
        with:
          host: example.com
          api_key: ${{ secrets.INDEX_NOW_API_KEY }}
          api_key_location: https://example.com/${{ secrets.INDEX_NOW_API_KEY }}.txt
          endpoint: yandex
          sitemap_locations: https://example.com/sitemap.xml
```

Learn more about the best practices for the [`secrets.INDEX_NOW_API_KEY` and other variables](https://jakob-bagterp.github.io/index-now-for-python/user-guide/github-actions/automated-workflows/).

[![IndexNow for Python source code on GitHub](https://img.shields.io/static/v1?label=GitHub&message=source%20code&logo=github&color=teal&link=https%3A%2F%2Fgithub.com%2Fjakob-bagterp%2Findex-now-submit-sitemap-urls-action)](https://github.com/jakob-bagterp/index-now-submit-sitemap-urls-action/)

[View on GitHub Marketplace](https://github.com/marketplace/actions/index-now-submit-sitemap-urls-action){ .md-button .md-button--secondary }

[Go to documentation](https://jakob-bagterp.github.io/index-now-submit-sitemap-urls-action/){ .md-button .md-button--primary }

## Timer for Python ⏳
Lightweight Python package that makes it easy to measure how much time it takes to run Python programs and gauge performance of multiple, smaller bits of code.

[![Downloads](https://static.pepy.tech/badge/timer-for-python)](https://pepy.tech/project/timer-for-python)
[![Timer for Python source code on GitHub](https://img.shields.io/static/v1?label=GitHub&message=source%20code&logo=github&color=teal&link=https%3A%2F%2Fgithub.com%2Fjakob-bagterp%2Ftimer-for-python)](https://github.com/jakob-bagterp/timer-for-python/)

[Go to documentation](https://jakob-bagterp.github.io/timer-for-python/){ .md-button .md-button--primary }

## Donations and How to Support the Projects 🏅
If you have already downloaded and tried any of the packages – maybe even used them in a production environment – perhaps you would like to support their development?

!!! tip "Become a Sponsor"
    If you find these projects helpful, please consider supporting its development. Your donations will help keep them alive and growing. Every contribution, no matter the size, makes a difference.

    [Donate on GitHub Sponsors](https://github.com/sponsors/jakob-bagterp){ .md-button .md-button--primary }

    Thank you for your support! 🙌
