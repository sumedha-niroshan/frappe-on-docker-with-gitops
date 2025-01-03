## Setup dev environment

# Configuration Guide for `apps.json`

This guide explains how to set up an `apps.json` file in `ci/sites.json` for managing your Frappe applications. 

## Creating the `apps.json` File

The `apps.json` file should contain repository links for your required Frappe applications. Below is an example configuration:

```json
[
    {
        "url": "https://github.com/frappe/erpnext",
        "branch": "version-15"
    },
    {
        "url": "https://github.com/frappe/payments",
        "branch": "version-15"
    },
    {
        "url": "https://github.com/frappe/hrms",
        "branch": "version-15"
    }
]
```

### Using Private Repositories

If you need to use private repositories, format the entries in the `apps.json` file as shown below:

```json
[
    {
        "url": "https://{USERNAME}:{ACCESS_TOKEN}@github.com/{repo}.git",
        "branch": "{BRANCH_NAME}"
    },
    {
        "url": "https://{USERNAME}:{ACCESS_TOKEN}@github.com/{repo}.git",
        "branch": "{BRANCH_NAME}"
    },
    {
        "url": "https://{USERNAME}:{ACCESS_TOKEN}@github.com/{repo}.git",
        "branch": "{BRANCH_NAME}"
    }
]
```

#### Replace the following placeholders with your information:
- `USERNAME`: Your GitHub username.
- `ACCESS_TOKEN`: Your GitHub personal access token. 
- `{repo}`: The repository name (e.g., `frappe/hrms`).
- `{BRANCH_NAME}`: The desired branch name (e.g., `version-15`).

#### Creating a GitHub Personal Access Token

Refer to the official GitHub documentation for instructions on generating a personal access token:
[Managing Your Personal Access Tokens](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens?source=post_page-----f3034be6d146--------------------------------)

## Environmental Configuration

Ensure your environmental variables are updated in the `ci/build.env` file. This file allows you to customize and manage build-specific configurations.

## Managing Versions

You can manage application versions using the `ci/version.txt` file, which should specify the required version for each application.

---

By following these steps, you can configure your `apps.json` file effectively and manage Frappe applications with ease.
