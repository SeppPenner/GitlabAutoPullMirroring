GitlabAutoPullMirroring
====================================

GitlabAutoPullMirroring is a script to update all Gitlab repositories to be mirrored from Github (Pull from Github, push is currently not possible: https://gitlab.com/gitlab-org/gitlab-ee/issues/7599).
Useful for all that are [#movingtogitlab](https://twitter.com/hashtag/movingtogitlab?lang=en). The script was written and tested in Python 3.7.1.

[![Build status](https://ci.appveyor.com/api/projects/status/dwyek279jpfod10i?svg=true)](https://ci.appveyor.com/project/SeppPenner/gitlabautopullmirroring)
[![GitHub issues](https://img.shields.io/github/issues/SeppPenner/GitlabAutoPullMirroring.svg)](https://github.com/SeppPenner/GitlabAutoPullMirroring/issues)
[![GitHub forks](https://img.shields.io/github/forks/SeppPenner/GitlabAutoPullMirroring.svg)](https://github.com/SeppPenner/GitlabAutoPullMirroring/network)
[![GitHub stars](https://img.shields.io/github/stars/SeppPenner/GitlabAutoPullMirroring.svg)](https://github.com/SeppPenner/GitlabAutoPullMirroring/stargazers)
[![GitHub license](https://img.shields.io/badge/license-AGPL-blue.svg)](https://raw.githubusercontent.com/SeppPenner/GitlabAutoPullMirroring/master/License.txt)

# Steps to use this script:
1. Migrate your projects from github to gitlab: https://docs.gitlab.com/ee/user/project/import/github.html
2. Wait until finished
3. Generate a personal access token on gitlab: https://docs.gitlab.com/ee/user/profile/personal_access_tokens.html
4. Get your user id from https://gitlab.com/profile or via 

![EditProfile](https://github.com/SeppPenner/GitlabAutoPullMirroring/blob/master/EditProfile.png "Edit profile") and
![GetUserId](https://github.com/SeppPenner/GitlabAutoPullMirroring/blob/master/UserId.png "Get user id")

4. Fill in your user name, user id and the generated access token in the following lines in the
[GitlabAutoPullMirroring.py](https://github.com/SeppPenner/GitlabAutoPullMirroring/blob/master/GitlabAutoPullMirroring.py) file:
```python
userName = "YourUserName"
userId = 1234567
token = "1234567890"
```

5. Install all required pip package dependencies with:
```python
pip install -r requirements.txt
```

6. Run the project using:
```bash
python GitlabAutoPullMirroring.py
```

or
```bash
./run.sh
```

# For more information see:
* https://docs.gitlab.com/ee/api/projects.html#start-the-pull-mirroring-process-for-a-project
* https://docs.gitlab.com/ee/api/projects.html#edit-project
* https://stackoverflow.com/questions/52428297/how-can-i-tell-gitlab-to-mirror-my-github-repositories-over-the-api/52443442#52443442
* https://stackoverflow.com/questions/52554811/how-can-i-change-the-mirroring-settings-in-gitlab-over-the-api/52554997#52554997
* https://gitlab.com/gitlab-org/gitlab-ee/issues/7599

Change history
--------------

* **Version 1.0.0.0 (2018-09-30)** : 1.0 release.