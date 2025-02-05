# Renovate Configurations

This repository contains shared configuration presets for [Renovate](https://docs.renovatebot.com/), a tool designed to automate the management of dependencies in software projects. By centralizing common Renovate configurations, this repository ensures consistent dependency management practices across multiple projects.

## Available Presets

The repository offers several predefined configuration presets tailored to different scenarios:

- **Default Configuration (`default.json`)**: Serves as the base configuration, encompassing standard settings applicable to most projects.
- **Automerge for Docker Digests (`automerge-docker-digest.json5`)**: Enables automatic merging of updates related to Docker image digests.
- **Automerge for GitHub Actions (`automerge-github-actions.json5`)**: Facilitates automatic merging of updates for GitHub Actions workflows.
- **Commit Message Convention (`commit-message.json5`)**: Defines a standardized format for commit messages to maintain consistency.
- **Custom Managers (`custom-managers.json5`)**: Configures custom package managers or extends support for additional languages and tools.
- **Pull Request Labels (`pr-labels.json5`)**: Specifies labels to be automatically applied to Renovate-generated pull requests for better categorization.
- **Semantic Commits (`semantic-commits.json5`)**: Enforces semantic versioning in commit messages to streamline release processes.

## Usage

To integrate these configurations into your project, follow these steps:

1. **Reference the Repository**:
   In your project's Renovate configuration file (commonly `renovate.json`), extend the desired preset from this repository. For example:

   ```json
   {
     $schema: "https://docs.renovatebot.com/renovate-schema.json",
     extends: [
         "local>rtrox/renovate-config"
      ],
   }
   ```

Replace default with the specific preset name if you wish to use a configuration other than the default.

Customize as Needed:
While the presets provide a solid foundation, you can further customize your Renovate settings within your project's configuration file to meet specific requirements.

## Benefits

Consistency: Ensures uniform dependency management across multiple projects by using shared configurations.
Efficiency: Reduces the need to define Renovate settings from scratch for each project, saving time and minimizing errors.
Maintainability: Centralized configurations make it easier to update and propagate changes across all projects that utilize these presets.
For more detailed information on configuring Renovate, please refer to the official Renovate documentation.
