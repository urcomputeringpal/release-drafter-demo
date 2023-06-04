# release-drafter-demo

A demo release workflow using https://github.com/marketplace/actions/release-drafter configured to create GitHub Releases in response to workflow_dispatch events. Releases can be created via the GitHub UI or the `gh` cli utility.

Release notes are automatically generated including PRs with the `Feature` or `Fix` label. PRs with the `Internal` or `Trivial` label are excluded. A 'require labels' workflow is required on all PRs to ensure all have one of the above labels. A header can be added to the release at creation time.

## Development workflow

- Create PRs against main

## Release Workflow

- Manually update the `release` branch: https://github.com/urcomputeringpal/release-drafter-demo/compare/release...main
- Create a release with the [releaser workflow](https://github.com/urcomputeringpal/release-drafter-demo/actions/workflows/releaser.yml), choosing the `release` ref:

<img width="338" alt="Screenshot 2023-06-04 at 8 58 41 AM" src="https://github.com/urcomputeringpal/release-drafter-demo/assets/47/2b3e4393-dab1-4c88-97f0-2b4dcf65a4da">

Results: https://github.com/urcomputeringpal/release-drafter-demo/releases

## Release Notifications

The official [GitHub Slack Integration](https://github.com/integrations/slack#customize-your-notifications) can be used to subscribe any channel to release notifications. All links in the release are clickable.

```
/github subscribe urcomputeringpal/release-drafter-demo releases
```

<img width="434" alt="image" src="https://github.com/urcomputeringpal/release-drafter-demo/assets/47/b042e80d-ae48-492f-b9a2-662321a475d2">
