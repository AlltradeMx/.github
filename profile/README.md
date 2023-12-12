# AllTradeMx Tech Rules

## Git Branch Strategy

We
used [Trunk-based development (TBD)](https://launchdarkly.com/blog/introduction-to-trunk-based-development/)
as the branching strategy.

![e.g][1]

The idea of this strategy is that all developers integrate their changes directly to a shared trunk
every day (in our case, our `main` branch), a shared trunk that is always in a releasable state. No
matter what a developer might do on their local repository, at least once each day, they must
integrate their code. This practice forces each developer to regularly see and react to the changes
being made by their teammates in version control, which drives collaboration around the quality and
state of the codebase as a near-constant activity.

### Branch Naming

In order to have a great administration with our branches, we have established a convention that
will allow us to identify them more quickly, the structure is as follows:

    type/username/short-description

Where

- `type`: The type of contribution you are about to make, we have at least 4.
    - `core`: Important changes to the project, an update in some fundamental part of the
      application, change in some configuration or addition of a specific library.
    - `feature`: Any new development that adds functionality to the project.
    - `fix`: The solution to a bug.
    - `release`: When bumping the `versionCode` and the `versionName` for the signature of a
      productive build.
- `username`: Your GitHub username.
- `short-description`: A brief description separated by `-` that help us to identify the objective
  of this branch.

**e.g.**

    feature/mariodev-at/add-new-feature


[1]: ../images/trunnkbasedevelopment.png
