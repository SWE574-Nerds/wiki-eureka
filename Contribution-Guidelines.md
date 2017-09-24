In this page you'll see details/expectations on

1. Steps for creating good issues or pull requests.
2. Links to external documentation, mailing lists, or a code of conduct.
3. Community and behavioral expectations.


## Creating Issues

We are using github Issues for tracking. Please take care that your issues adheres to these rules.
1. Provide an informative and short title.
2. Give out as many details as you can in message body.
3. Describe your issue with a general sense if possible, not specific to a situation.
4. Provide any detail that we need to have to understand your request in the issue body. (no links to your blog etc.) 
5. Any support material (visuals, videos) is welcome!

## Pull requests

There are two way to create your pull request.
### Via Github

1. Fork this repository.
2. Make your changes on your copy of the repository.
3. On GitHub page, create a Pull request to this repository "master" branch.

### Via E-mail

This option requires a certain level of understanding of git but is useful for people that don't have a GitHub account.
1. clone this repository 
2. Make your changes directly on master branch
3. create patches from your local repository using:

     `git format-patch HEAD...origin/master -o patches/`

4. Send these patches to any of the contributors/active maintainers of this project. You can do this by 
  a. git-send-email (You need to setup git for email. [git-send-email](https://git-scm.com/docs/git-send-email), [smtp on git](https://www.freedesktop.org/wiki/Software/PulseAudio/HowToUseGitSendEmail/))

        `git send-email patches/*.patch # (You'll be prompted to fill in details)`

  b. Any email sending client. (Be sure to send in plain-text mode as HTML formatting and encoding differences will corrupt your patches)
After you've sent your patches, the reviewer will add these to the repository after code review.

## Some tips on commits
1. Please be crystal clear in your commit messages.
2. Please create commits per change. (i.e. don't bundle many changes in a commit and name it after just by one)


## Want to Contribute?
That's great! Please keep an eye on our Issues list and product roadmap, and feel free to contact us!
