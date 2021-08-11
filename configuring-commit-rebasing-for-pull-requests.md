---
title: Configuring commit rebasing for pull requests
intro: 'You can enforce, allow, or disable commit rebasing for all pull request merges on {% data variables.product.product_location %} in your repository.'
redirect_from:
  - /articles/configuring-commit-rebasing-for-pull-requests
  - /github/administering-a-repository/configuring-commit-rebasing-for-pull-requests
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
topics:
  - Repositories
shortTitle: Configure commit rebasing
---

3. Under "Merge button", select **Allow rebase merging**. This allows contributors to merge a pull request by rebasing their individual commits onto the base branch. If you also select another merge method, collaborators will be able to choose the type of merge commit when merging a pull request. {% data reusables.repositories.squash-and-rebase-linear-commit-hisitory %}
![Pull request rebased commits](/assets/images/help/repository/pr-merge-rebase.png)
Reference: https://github.com/github/docs/blob/main/content/github/administering-a-repository/configuring-pull-request-merges/configuring-commit-rebasing-for-pull-requests.md