This is a bit of a mystery, but publishing a site is not as simple as just pushing files to the remote repo.

I think this involves CI

And as the repos are currently set up, the CI config expects to see a load of stuf about Mkdocs, so if you want to use flat html, you must set it up differently

Here's a CI file for a flat HTML site:

https://gitlab.fabcloud.org/academany/fabacademy/2021/labs/barcelona/site/-/blob/master/.gitlab-ci.yml

```.gitlab-ci.yml```

```# This file is a template, and might need editing before it works on your project.
# Full project: https://gitlab.com/pages/plain-html
pages:
  stage: deploy
  script:
    - mkdir .public
    - cp -r * .public
    - mv .public public
  artifacts:
    paths:
      - public
  only:
    - master
```
