# Git 1

---

## Git

Git is the ultimate version control system or source code management that widely used by various people in the world.

Mostly used by developers to manage their projects and collaborate with others.

### Installation

```sh
# on ubuntu
sudo apt install git tig
# on mac
brew install git tig
```

## Commands

Some basic Git commands are

`config`, `init`, `clone`, `status`, `add`, `commit`, `log`, `checkout`, `remote`, `push`, `pull`

Firstly after we installed Git in our computer, we should `config` it first with our name and email.

```sh
$ git config --global user.name "Your Full Name"
$ git config --global user.email "yourname@example.com"
```

We can initialize a new repo in an existing folder.

```sh
git init
```

After initialization, let's see the repo status.

```sh
git status
```

We would like to create a new file, then add it into our repo.

```sh
$ ls
README.md
index.html

$ git add README.md index.html
```

Then commit them with a message

```sh
$ git commit -m "Create README and HTML page"
```

See the changes log as well.

```sh
$ git log
```

---

## GitHub

[GitHub](https://github.com) is the most popular platform to publish and collaborate on Git repositories.

The followings are getting started step to use GitHub.

1.  Register for a new user account
2.  Edit your user profile
3.  Create and manage repository on GitHub
4.  Initialize README & license on the repo
5.  Be invited to existing organization
6.  Explore Open Source world on GitHub

Or better yet, there's [GitHub Learning Lab](https://lab.github.com):

Get the skills you need without leaving GitHub. GitHub Learning Lab takes you through a series of fun and practical projects, sharing helpful feedback along the way.

* [GitHub Learning Lab - YouTube](https://www.youtube.com/watch?v=9S0p8YMQzsM)
  * [GitHub Learning Lab: Introduction to GitHub Walkthrough](https://www.youtube.com/watch?v=sz6zfrQpCQg&list=PLg7s6cbtAD147DXcVp899Fk6SegoLY9gL)
* [GitHub Learning Lab Courses](https://lab.github.com/courses)

You can also install GitHub mobile apps:

* Android
  * [PocketHub](https://play.google.com/store/apps/details?id=com.github.pockethub.android)
  * [GitPoint](https://play.google.com/store/apps/details?id=com.gitpoint)
  * [FastHub](https://play.google.com/store/apps/details?id=com.fastaccess.github)
* iOS
  * [Working Copy - Powerful Git client](https://itunes.apple.com/us/app/working-copy/id896694807)
  * [GitPoint for GitHub - A complete GitHub client](https://itunes.apple.com/us/app/gitpoint-for-github/id1251245162)
  * [CodeHub - A Client for GitHub](https://itunes.apple.com/us/app/codehub-a-client-for-github/id707173885)

## Syncing Repo with GitHub

After creating a repo on GitHub, push the changes to the remote upstream.

```sh
$ git remote add origin git@github.com:impactbyte-learn/hello-world.git
$ git push -u origin master
```

When we want to push any changes later on, just use push right away.

```sh
$ git push
```

To get updates, pull it.

```sh
$ git pull
```

---

## GitLab

[GitLab](https://gitlab.com) is GitHub alternative that is free for private projects.

There's even the [mobile app](https://play.google.com/store/apps/details?id=com.commit451.gitlab).

---

## GitBook

[GitBook](https://www.gitbook.com) is a free tool to create book or documentation using Git repo.

---

## References

* [Git Handbook · GitHub Guides](https://guides.github.com/introduction/git-handbook)
