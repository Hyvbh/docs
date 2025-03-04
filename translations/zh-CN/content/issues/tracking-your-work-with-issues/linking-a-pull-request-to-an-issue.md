---
title: 将拉取请求链接到议题
intro: 您可以将拉取请求链接到议题，以显示修复正在进行中，并在拉取请求被合并时自动关闭该议题。
redirect_from:
  - /github/managing-your-work-on-github/managing-your-work-with-issues-and-pull-requests/linking-a-pull-request-to-an-issue
  - /articles/closing-issues-via-commit-message
  - /articles/closing-issues-via-commit-messages
  - /articles/closing-issues-using-keywords
  - /github/managing-your-work-on-github/closing-issues-using-keywords
  - /github/managing-your-work-on-github/linking-a-pull-request-to-an-issue
  - /issues/tracking-your-work-with-issues/creating-issues/linking-a-pull-request-to-an-issue
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - Pull requests
shortTitle: 将 PR 链接到议题
---

{% note %}

**注：**当拉取请求指向仓库的*默认*分支时，将解析拉取请求说明中的特殊关键字。 但是，如果拉取请求的基础是*任何其他分支*，则将忽略这些关键字，不创建任何链接，并且合并拉取请求对议题没有影响。 **如果要使用关键字将拉取请求链接到议题，则拉取请求必须在默认分支上。**

{% endnote %}

## 关于链接的议题和拉取请求

You can link an issue to a pull request manually or using a supported keyword in the pull request description.

当您将拉取请求链接到拉取请求指向的议题，如果有人正在操作该议题，协作者可以看到。

将链接的拉取请求合并到仓库的默认分支时，其链接的议题将自动关闭。 有关默认分支的更多信息，请参阅“[更改默认分支](/github/administering-a-repository/changing-the-default-branch)”。

## 使用关键词将拉取请求链接到议题

您可以通过在拉取请求说明或提交消息中使用支持的关键词将拉取请求链接到议题。 拉取请求**必须**在默认分支上。

* close
* closes
* closed
* fix
* fixes
* fixed
* 解决
* resolves
* resolved

如果使用关键字在另一个拉取请求中引用拉取请求注释，则将链接拉取请求。 合并引用拉取请求也会关闭引用的拉取请求。

关闭关键词的语法取决于议题是否与拉取请求在同一仓库中。

| 链接的议题    | 语法                                            | 示例                                                             |
| -------- | --------------------------------------------- | -------------------------------------------------------------- |
| 同一仓库中的议题 | *KEYWORD* #*ISSUE-NUMBER*                     | `Closes #10`                                                   |
| 不同仓库中的议题 | *KEYWORD* *OWNER*/*REPOSITORY*#*ISSUE-NUMBER* | `Fixes octo-org/octo-repo#100`                                 |
| 多个议题     | 对每个议题使用完整语法                                   | `Resolves #10, resolves #123, resolves octo-org/octo-repo#100` |

Only manually linked pull requests can be manually unlinked. To unlink an issue that you linked using a keyword, you must edit the pull request description to remove the keyword.

您也可以在提交消息中使用关闭关键词。 议题将在提交合并到默认分支时关闭，但包含提交的拉取请求不会列为链接的拉取请求。

## 手动将拉取请求链接到议题

对仓库有写入权限的任何人都可以手动将拉取请求链接到议题。

您可以手动链接最多 10 个议题到每个拉取请求。 议题和拉取请求必须位于同一仓库中。

{% data reusables.repositories.navigate-to-repo %}
{% data reusables.repositories.sidebar-pr %}
3. 在拉取请求列表中，单击要链接到议题的拉取请求。
{% ifversion fpt or ghec or ghes > 3.4 or ghae-issue-6234 %}
4. 在右侧边栏的“Development（开发）”部分，单击 {% octicon "gear" aria-label="The Gear icon" %}。
{% else %}
4. 在右侧边栏中，单击 **Linked issues（链接的议题）**。 ![右侧边栏中链接的议题](/assets/images/help/pull_requests/linked-issues.png)
{% endif %}
5. 单击要链接到拉取请求的议题。 ![下拉以链接议题](/assets/images/help/pull_requests/link-issue-drop-down.png)

## 延伸阅读

- "[自动链接的引用和 URL](/articles/autolinked-references-and-urls/#issues-and-pull-requests)"
