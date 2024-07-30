# Issue Manager GitHub Action

This GitHub Action creates issues based on the completeness of the Code of Conduct in a repository.

## Features

- Creates an issue if the Code of Conduct is detected to be incomplete.
- Creates an issue if specific guidelines are missing from the Code of Conduct.
- Customizable issue creation based on different event actions.

## Inputs

- `repo_name` **(required)**: The name of the repository where the issue will be created.
- `bot_token` **(required)**: GitHub token for authentication as the bot user.
- `event_action` **(required)**: The action to determine which type of issue to create.
- `missing_flags` **(optional)**: A comma-separated list of missing guidelines flags.

### How It Works
1. **Create Issue for Incomplete Code of Conduct**: 
   - If the `event_action` is `code_of_conduct_incomplete`, an issue is created indicating that the current Code of Conduct is incomplete.
   - The issue body highlights the need for more detailed guidelines to ensure a comprehensive Code of Conduct.

2. **Create Issue for Missing Guidelines**: 
   - If the `event_action` is `create_issue_for_missing_guidelines`, an issue is created listing specific guidelines that are missing.
   - The issue body is dynamically generated based on the missing flags provided, suggesting enhancements for positive behavior and highlighting unacceptable behavior.

## Example Scenario
- **Incomplete Code of Conduct**: The action creates an issue with a message indicating that the Code of Conduct is incomplete and requires more details.
- **Missing Specific Guidelines**: The action creates an issue listing specific missing guidelines and suggests incorporating them to enhance the Code of Conduct.

## Permissions
This action requires the following permissions:

- `issues: write`
- `contents: write`

Ensure these permissions are set in your workflow.

## License
This work is licensed under a Creative Commons Attribution-ShareAlike 4.0 International License.

The CC BY-SA license allows users to distribute, remix, adapt, and build upon the material in any medium or format, so long as attribution is given to the creator. The license allows for commercial use. If you remix, adapt, or build upon the material, you must license the modified material under identical terms.

[Creative Commons License](https://creativecommons.org/licenses/by-sa/4.0/)

## Author
Created by CobosDS. For any issues or contributions, please open an issue or submit a pull request on the [GitHub repository](https://github.com/SOM-Research/issue-manager).
