---
title: "Composer 2.9.8 and 2.2.28 fix GitHub Actions token disclosure in error messages"
url: "https://blog.packagist.com/composer-2-9-8-and-2-2-28-fix-github-actions-token-disclosure-in-error-messages/"
date: "2026-05-13"
author: "Nils Adermann"
feed_url: "https://blog.packagist.com/feed/"
---
Please immediately update Composer to version 2.9.8 or 2.2.28 (LTS) by running composer.phar self-update . The new releases fix a vulnerability where Composer leaks the full contents of GitHub Actions issued GITHUB_TOKEN s or GitHub App installation tokens to the GitHub Actions logs. GitHub
