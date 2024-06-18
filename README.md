# RSS-GPT

[![](https://img.shields.io/github/last-commit/yinan-c/RSS-GPT/dev?label=updated)](https://github.com/yinan-c/RSS-GPT/tree/dev)
[![](https://img.shields.io/github/last-commit/yinan-c/RSS-GPT/main?label=feeds%20refreshed)](https://yinan-c.github.io/RSS-GPT/)
[![](https://img.shields.io/github/license/yinan-c/RSS-GPT)](https://github.com/yinan-c/RSS-GPT/blob/master/LICENSE)


## What is this?

[Configuration Guide](https://yinan-c.github.io/rss-gpt-manual-en.html) | [中文简介](README-zh.md) | [中文教程](https://yinan-c.github.io/rss-gpt-manual-zh.html)

Using GitHub workflow to run a simple Python script repeatly, Calling OpenAI API to generate summaries for RSS feeds, and then push the generated feeds to GitHub Pages. Easy to configure, no server needed.

### Features

- Use ChatGPT to summarize RSS feeds, and attach summaries to the original articles, support custom summary length and target language.
- Aggregate multiple RSS feeds into one, remove duplicate articles, subscribe with a single address.
- Add filters to your own personalized RSS feeds.
- Host your own RSS feeds on GitHub repo and GitHub Pages.

![](https://i.imgur.com/7darABv.jpg)

## Quick configuration guide

- Fork this repo
- Add Repository Secrets
    - U_NAME: your GitHub username
    - U_EMAIL: your GitHub email
    - WORK_TOKEN: your GitHub personal accesstoken with `repo` and `workflow` scope, get it from [GitHub settings](https://github.com/settings/tokens/new)
    - OPENAI_API_KEY(OPTIONAL, only needed when using AI summarization feature): Get it from [OpenAI website](https://platform.openai.com/account/api-keys)
- Enable GitHub Pages in repo settings, choose GitHub Actions as the source
- Configure your RSS feeds in config.ini

You can check out [here](https://yinan-c.github.io/rss-gpt-manual-en.html) for a more detailed configuration guide.

## ChangeLog and updates

- There is a [`dev` branch](https://github.com/yinan-c/RSS-GPT/tree/dev) for manual updates on the script, auto commits will no longer be pushed to this `dev` branch. The purpose of doing this is to separate the manual updates and auto commits, so that it is easier to check the updates and pull to your repo.
- Check out the [CHANGELOG.md](CHANGELOG.md).

## Example feeds being processed

These feeds on hosted in the [`doc/` subdirectory](https://github.com/yinan-c/RSS-GPT/tree/main/docs) in this repo as well as on my [GitHub Pages](https://yinan-c.github.io/RSS-GPT/). Feel free to subscribe in your favorite RSS reader.

I will consider hosting more feeds in the future. Email me or submit an issue if there is any question using the script or any suggestions.
- https://rss-hub-red-two.vercel.app/telegram/channel/tnews365, https://rss-hub-red-two.vercel.app/telegram/channel/times001, https://rss-hub-red-two.vercel.app/telegram/channel/OutsightChina, https://chinadigitaltimes.net/chinese/feed -> https://samuelshi.github.io/RSS/DailyNews.xml
- https://bloombergnew.buzzing.cc/feed.xml, https://china.buzzing.cc/feed.xml, https://depth.buzzing.cc/feed.xml, https://economistnew.buzzing.cc/feed.xml, https://atlantic.buzzing.cc/feed.xml -> https://samuelshi.github.io/RSS/Buzzing.xml
- https://rsshub.bytegeniuses.com/telegram/channel/NewlearnerChannel, https://rsshub.bytegeniuses.com/telegram/channel/jike_collection, https://rsshub.bytegeniuses.com/telegram/channel/xhqcankao, https://rsshub.bytegeniuses.com/telegram/channel/AppleNuts -> https://samuelshi.github.io/RSS/DailyTech.xml
- https://rsshub.bytegeniuses.com/telegram/channel/appinnfeed -> https://samuelshi.github.io/RSS/Appinn.xml
- https://rsshub.app/twitter/user/whyyoutouzhele, https://rsshub.app/twitter/user/xiaojingcanxue, https://rsshub.app/twitter/user/fangshimin, https://rsshub.app/twitter/user/caiziboshi, https://rsshub.app/twitter/user/wangzhian8848 -> https://samuelshi.github.io/RSS/Twitter.xml
