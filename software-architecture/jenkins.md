[Large-Scale Continuous Delivery at Netflix and Waze Using Spinnaker](https://www.youtube.com/watch?time_continue=12&v=PLNheBiWOGI)

[30 Jenkins features and plugins you wished you had known about before](https://www.youtube.com/watch?v=6BIry0cepz4)

[aking Jenkins Pipeline to the Extreme](https://www.youtube.com/watch?v=LgcYertiI70)

[Adopting DevOps? You Are Aiming at the Wrong Target!](https://www.infoq.com/presentations/devops-transforming-it)


[Injecting Secrets into Jenkins Build Jobs
](https://support.cloudbees.com/hc/en-us/articles/203802500-Injecting-Secrets-into-Jenkins-Build-Jobs)

[Storing Secrets ](https://jenkins.io/doc/developer/security/secrets/)

[Using credentials](https://jenkins.io/doc/book/using/using-credentials/)

[Credentials Plugin](https://wiki.jenkins.io/display/JENKINS/Credentials+Plugin)

["these days I care about continuous delivery a lot more than technology choice or programming language"](https://twitter.com/thumphriees/status/1054480904167419905).

[30 Jenkins features and plugins you wished you had known about before!](https://www.youtube.com/watch?v=6BIry0cepz4).

[Jenkins is Getting Old](https://itnext.io/jenkins-is-getting-old-2c98b3422f79). [hn](https://news.ycombinator.com/item?id=19781251).

[CI/CD for Kubernetes With Jenkins and Spinnaker (Part 2)](https://dzone.com/articles/cicd-for-kubernetes-with-jenkins-and-spinnaker-con)

[GitHub Actions now supports CI/CD, free for public repositories](https://news.ycombinator.com/item?id=20646350)

[Modern Continuous Delivery • Ken Mugrage](https://www.youtube.com/watch?v=w008iz_UwDk&list=PLEx5khR4g7PKT9RvuVyQxJLO8CZUJzNMy&index=25)

[Introduction to GitOps with OpenShift](https://blog.openshift.com/introduction-to-gitops-with-openshift/)

[Bazel 2.0 Released](https://news.ycombinator.com/item?id=21863393)

[supply chain tools like Grafeas, Kritis, in-toto, Clair, Micro Scanner, TUF, and Notary](https://twitter.com/JAXenterCOM/status/1223272225127780355)

[CI/CD for Databases talk](https://twitter.com/jbogard/status/1223262501544087552)

[haskell ci cd](https://www.reddit.com/r/haskell/comments/eykyzf/what_is_your_haskell_cicd_like_in_2020/)

[Automating a Software Company with GitHub Actions](https://news.ycombinator.com/item?id=28234057)

[Automating Fourmolu releases with GitHub Actions](https://brandonchinn178.github.io/blog/2022/05/19/automating-fourmolu-releases-with-github-actions.html)

[About [GitHub] workflows](https://docs.github.com/en/actions/using-workflows/about-workflows). [example](https://github.com/github/darrrr/actions/runs/39771470/workflow).

> The run keyword tells the job to execute a command on the runner.

    run: |
      sudo apt-get install libsqlite3-dev

[Fast builds, secure builds. Choose two.](https://stripe.com/blog/fast-secure-builds-choose-two)

[A Deep Dive into GitHub Actions’ Reusable Workflows](https://betterprogramming.pub/how-to-use-github-actions-reusable-workflow-8604e8cbf258)

[Introducing required workflows and configuration variables to GitHub Actions](https://github.blog/2023-01-10-introducing-required-workflows-and-configuration-variables-to-github-actions/)

[What is the github action paths-ignore equivalent in buildkite?](https://forum.buildkite.community/t/what-is-the-github-action-paths-ignore-equivalent-in-buildkite/2045)

[GA common actions](https://ashishb.net/tech/common-pitfalls-of-github-actions/)

[The Hidden Cost of Parallel Processing in GitHub Actions](https://betterprogramming.pub/the-hidden-cost-of-parallel-processing-in-github-actions-63f25b2d5f6a)

[managing pipeline secrets](https://buildkite.com/docs/pipelines/secrets). [agent hooks](https://buildkite.com/docs/agent/v3/hooks#hook-locations-agent-hooks)

[Your CI/CD pipeline should start on the developer's laptop](https://twitter.com/solomonstre/status/1649118014594502656)

[Job retries in Buildkite](https://buildkite.com/blog/job-retries)

[Don’t Configure Control Flow](https://lobste.rs/s/ycj1l5/don_t_configure_control_flow)

[Cache plugin for buildkite?](https://forum.buildkite.community/t/cache-plugin-for-buildkite/1324)

[Continuous Integration](https://martinfowler.com/articles/continuousIntegration.html)

[GA - adding to system path](https://docs.github.com/en/actions/using-workflows/workflow-commands-for-github-actions#adding-a-system-path)

[GA - RUNNER_TEMP](https://docs.github.com/en/actions/learn-github-actions/variables)

[Buildkite metadata](https://forum.buildkite.community/t/need-clarification-on-meta-data-usage-pattern/762)

> Meta-data is intended for simple pieces of key/value data that you want to use to identify or filter your builds. It can be used to filter results when looking at a list of builds on buildkite.com, when using the builds api, or to transport small values between jobs in the same build using the agent meta-data commands 3.

[How call rest api in command step in buildkite?](https://stackoverflow.com/questions/76983485/how-call-rest-api-in-command-step-in-buildkite)

[Exporting Buildkite settings with environment hooks](https://buildkite.com/docs/pipelines/secrets#exporting-secrets-with-environment-hooks)

[Run your GitHub Actions workflow on a schedule](https://jasonet.co/posts/scheduled-actions/). [Events that trigger workflows](https://docs.github.com/en/actions/using-workflows/events-that-trigger-workflows). [the schedule event](https://docs.github.com/en/actions/using-workflows/events-that-trigger-workflows#schedule)

> The schedule event allows you to trigger a workflow at a scheduled time.

> Scheduled workflows run on the latest commit on the default or base branch.

> A single workflow can be triggered by multiple schedule events. You can access the schedule event that triggered the workflow through the github.event.schedule context. 

[GitHub actions contexts](https://docs.github.com/en/actions/learn-github-actions/contexts)

[Buildkite - defining your pipeline steps](https://buildkite.com/docs/pipelines/defining-steps). [file](https://buildkite.com/docs/pipelines/defining-steps#step-defaults-pipeline-dot-yml-file).

> Pipeline steps are defined in YAML and are either stored in Buildkite or in your repository using a pipeline.yml file.

[Buildkite - Trigger step](https://buildkite.com/docs/pipelines/trigger-step)

> A trigger step creates a build on another pipeline.

[Buildkite - Shallow clones? (2019)](https://forum.buildkite.community/t/shallow-clones/282). [blobless clones, treeless clones, shallow clones](https://github.blog/2020-12-21-get-up-to-speed-with-partial-clone-and-shallow-clone/). 

> BUILDKITE_GIT_CLONE_FLAGS

> it seems that the clone process is only in the beginning when our yml gets loaded and after that its only fetching the repo.

> Blobless clones definitely feel much faster than full clones, and don’t have the broken-history problem that a shallow clone has (blobs are fetched on-demand, but the full commit history is present).

> Treeless clones are mentioned as being useful for CI builds in which you’re throwing away the clone after the build

> git clone --filter=tree:0 <url> creates a treeless clone. These clones download all reachable commits while fetching trees and blobs on-demand. These clones are best for build environments where the repository will be deleted after a single build, but you still need access to commit history.

[cache-buildkite-plugin](https://github.com/buildkite-plugins/cache-buildkite-plugin)

[Git clone flags in the agent configuration](https://buildkite.com/docs/agent/v3/configuration#git-clone-flags)

[Buildkite - Pre-checkout. clone another repo](https://forum.buildkite.community/t/pre-checkout-clone-another-repo/2053)

[timeouts and CI](https://twitter.com/joseph_h_garvin/status/1784380166342332657)

[[r/devops] How Do You Handle Rollbacks in CI/CD Pipelines?](https://www.reddit.com/r/devops/comments/1fnh7qp/how_do_you_handle_rollbacks_in_cicd_pipelines/)


