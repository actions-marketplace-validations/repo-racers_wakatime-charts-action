<a href="https://reporacers.com/" taarget="_blank">
  <img src="https://github.com/repo-racers/.github/blob/main/profile/repo-racers.svg" alt="Repo Raacers" width="600px"/>
</a>

This repository is included in our open-source Pro Support service which offers an efficient solution for managing popular GitHub Actions dependencies with ease:

🙌 forked from [dvjn/wakatime-charts](https://github.com/dvjn/wakatime-charts)

<details>

<summary>What is Open-Source Pro Support?</summary>

Open-Source Pro Support is a comprehensive service designed to streamline your workflow by providing:

- **Customized Forks:** We create public forks of popular GitHub Actions, ensuring you have access to the latest features and fixes.
  
- **Dedicated Technical Support:** Say goodbye to the hassle of managing multiple open-source dependencies. With our service, you have a single point of contact for all your support needs. Reach out to us on our [Discord](https://discord.com/channels/1229786735161118882/1229786735161118885) server, and our team of experts will be ready to assist you.
  
- **Priority Fixes:** Experience seamless issue resolution with our priority fix service. If you encounter any issues with our forks, we prioritize fixing them promptly to minimize disruptions to your workflow.
  
- **Community Contribution:** We believe in giving back to the open-source community. When we fix issues in our forks, we handle creating pull requests to the original authors, ensuring that the entire community benefits from the improvements.

</details>

<details>

<summary>How It Works</summary>


1. **Choose Our Fork:** Instead of referencing popular GitHub Actions repositories directly, simply reference this repository in your workflow.
   
2. **Enjoy Dedicated Support:** If you encounter any issues or need assistance, reach out to us on our [Discord](https://discord.com/channels/1229786735161118882/1229786735161118885) server. Our team will be happy to help you promptly.
   
3. **Benefit from Priority Fixes:** Experience seamless issue resolution with our priority fix service. We prioritize fixing issues in our forks to ensure smooth operation for your projects.
   
4. **Contribute to the Community:** Rest assured that when we fix issues in our forks, we contribute back to the original repositories, benefiting the entire open-source community.

*Not Your Thing?*

We don't want to get in between you and the community. If you want to handle forking and submitting a pull request yourself, that's awesome.

However, feel free to reach out to us on [Discord](https://discord.com/channels/1229786735161118882/1229786735161118885) anyway if you need any help and advice in doing so.

:heart: [open-source](https://opensource.org/)

</details>

---

<div align="center">

![Weekly Language Stats](https://raw.githubusercontent.com/dvjn/wakatime-charts/master/images/wakatime_weekly_language_stats.svg "Weekly Language Stats")
![Weekly Project Stats](https://raw.githubusercontent.com/dvjn/wakatime-charts/master/images/wakatime_weekly_project_stats.svg "Weekly Project Stats")

</div>

## How to Use 🚀

### Set it up in your repository ⚙️

1. Add your wakatime api key from [here](https://wakatime.com/settings/api-key), in your repository secrets with the name `WAKATIME_API_KEY`.

2. **Optional:** If you are adding this action to a repository other than your profile repository (`<username>/<username>`), add your Github API Token from [here](https://github.com/settings/tokens), in your repository secrets with the name `GITHUB_TOKEN`.

3. Go to actions tab of your repository, click `New workflow`, and then click the link `set up a workflow yourself`.

4. Replace all the file contents with the following:

   ```yaml
   name: Wakatime Charts

   on:
     workflow_dispatch:
     schedule:
       - cron: "0 0 * * *"

   jobs:
     update-charts:
       name: Update wakatime stats charts
       runs-on: ubuntu-latest
       steps:
         - uses: repo-racers/wakatime-charts-action@[insert version or commit]
           with:
             WAKATIME_API_KEY: ${{ secrets.WAKATIME_API_KEY }}
             GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }} # only required if using the action in repository other than profile
   ```

5. Commit this workflow file.

**Note:** The action will run at 00:00 UTC everyday to update the images.

### Other Parameters 🔧

- `BRANCH_NAME`: Set the branch on which charts are pushed. Defaults to `master`
- `COMMIT_MESSAGE`: Set the commit message for the changes. Defaults to `📊`
- `IMAGES_FOLDER`: Set the folder name in which generated images are stored. Defaults to `images`
- `GIT_USER_EMAIL`: Set the user email for git config. Defaults to Github Action Bot's email `41898282+github-actions[bot]@users.noreply.github.com`
- `GIT_USER_NAME`: Set the user name for git config. Defaults to `Github Action`

### Using generated images 🔗

Link for the generated images is:
`https://raw.githubusercontent.com/<username>/<repository>/<branch_name>/<images_folder>/<chart_name>.svg`

Where, the chart name is one of `wakatime_weekly_language_stats` and `wakatime_weekly_project_stats`.

## Inspiration 😍

- [wakatime-readme](https://github.com/marketplace/actions/waka-readme)
- [Profile-Readme-WakaTime](https://github.com/marketplace/actions/wakatime-stat-update-action)
- [github-readme-stats](https://github.com/anuraghazra/github-readme-stats)

---

> [!TIP]
> For support with this repo and many other open-source projects, visit us at https://reporacers.com/ and join us on  [Discord](https://discord.com/channels/1229786735161118882/1229786735161118885).